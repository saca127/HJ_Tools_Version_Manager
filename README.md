# HJ Tools – Version Manager

Kênh phát hành công khai cho các tool của HJ. Repo này **chỉ chứa bản build**, không chứa mã nguồn.

## Danh sách tool

| app_id | Tool | Tải bản mới nhất |
|---|---|---|
| `auto-read-drive` | Auto Read GGDrive (Drive Data Extractor) | [Releases](https://github.com/saca127/HJ_Tools_Version_Manager/releases?q=auto-read-drive) |

## Quy ước

- Tag release: `<app_id>-v<version>`, ví dụ `auto-read-drive-v1.8`.
- Link tải cố định: `https://github.com/saca127/HJ_Tools_Version_Manager/releases/download/<app_id>-v<version>/<file>`.
- `tools/<app_id>/version.json`: thông tin phiên bản mới nhất của từng tool (nguồn dự phòng).
- Danh bạ phiên bản chính nằm trong Google Sheet **HJ_Tools_Version_Manager** (tab `Versions`), app đọc qua Apps Script webhook `?app=<app_id>`.

## Thêm tool mới

1. Thêm một dòng vào tab `Versions` của Sheet (`app_id`, `version`, `name`, `download_url`, `changelog`, `exp`).
2. Tạo release với tag `<app_id>-v<version>` và đính kèm file build.
3. Tạo `tools/<app_id>/version.json`.

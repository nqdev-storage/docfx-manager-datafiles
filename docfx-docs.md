---
title: DocFX Docs
description: DocFX Docs description
---

> [!NOTE]
> Information the user should notice even if skimming.

[!INCLUDE [my-markdown-block](./includes/my-markdown-block.md)]

## Markdown

[Markdown](https://daringfireball.net/projects/markdown/) là ngôn ngữ đánh dấu nhẹ với cú pháp định dạng văn bản đơn giản. Docfx hỗ trợ phân tích cú pháp Markdown tuân thủ [CommonMark](https://commonmark.org/) thông qua công cụ phân tích cú pháp [Markdig](https://github.com/xoofx/markdig).

### [YAML header](#tab/yaml-header)

Còn được gọi là YAML Front Matter, tiêu đề YAML được sử dụng để chú thích tệp Markdown với các thành phần siêu dữ liệu khác nhau.

### [Tabs](#tab/tabs)

Tab cho phép nội dung có nhiều mặt. Chúng cho phép các phần của tài liệu chứa các kết xuất nội dung biến thể và loại bỏ nội dung trùng lặp.

---

## Table of Contents

Mục lục (TOC) xác định cấu trúc của một bộ tài liệu.

### [YAML TOC](#tab/yaml-toc)

Để thêm TOC, hãy tạo một tệp có tên `toc.yml`. Đây là cấu trúc của YAML TOC đơn giản:

```yaml
items:
  - name: Tutorial
    items:
      - href: tutorial.md
      - href: step-1.md
      - href: step-2.md
      - href: step-3.md
```

---

## Config

Docfx sử dụng `docfx.json` làm tệp cấu hình cho trang web. Hầu hết các lệnh docfx hoạt động trong thư mục chứa `docfx.json`.

---

## Template

Mẫu xác định diện mạo của trang web. DocFX cung cấp một số mẫu dựng sẵn. Chúng tôi khuyên bạn nên sử dụng mẫu hiện đại phù hợp với giao diện của trang web này. Nó hỗ trợ chế độ tối, nhiều tính năng hơn, tùy chọn tùy chỉnh phong phú và.

### Template Metadata

Cách dễ nhất để tùy chỉnh giao diện của trang là sử dụng [siêu dữ liệu](https://dotnet.github.io/docfx/docs/config.html#metadata). Dưới đây là danh sách siêu dữ liệu được xác định trước:

#### [Modern Template](#tab/modern)

| Name                    | Type   | Description                                                                             |
| ----------------------- | ------ | --------------------------------------------------------------------------------------- |
| `_appTitle`             | string | A string append to every page title.                                                    |
| `_appName`              | string | The name of the site displayed after logo.                                              |
| `_appFooter`            | string | The footer HTML.                                                                        |
| `_appLogoPath`          | string | Path to the app logo.                                                                   |
| `_appLogoUrl`           | string | URL for the app logo.                                                                   |
| `_appFaviconPath`       | string | Favicon URL path.                                                                       |
| `_enableSearch`         | bool   | Whether to show the search box.                                                         |
| `_noindex`              | bool   | Whether to include in search results                                                    |
| `_disableContribution`  | bool   | Whether to show the _"Edit this page"_ button.                                          |
| `_gitContribute`        | object | Defines the `repo` and `branch` property of git links.                                  |
| `_gitUrlPattern`        | string | URL pattern of git links.                                                               |
| `_disableNewTab`        | bool   | Whether to render external link indicator icons and open external links in a new tab.   |
| `_disableNavbar`        | bool   | Whether to show the navigation bar.                                                     |
| `_disableBreadcrumb`    | bool   | Whether to show the breadcrumb.                                                         |
| `_disableToc`           | bool   | Whether to show the TOC.                                                                |
| `_disableAffix`         | bool   | Whether to show the right rail.                                                         |
| `_disableNextArticle`   | bool   | Whether to show the previous and next article link.                                     |
| `_disableTocFilter`     | bool   | Whether to show the table of content filter box.                                        |
| `_googleAnalyticsTagId` | string | Enables Google Analytics web traffic analysis.                                          |
| `_lang`                 | string | Primary language of the page. If unset, the `<html>` tag will not have `lang` property. |
| `_layout`               | string | Determines the layout of the page. Supported values are `landing` and `chromeless`.     |

#### [Default Template](#tab/default)

| Name                    | Type   | Description                                                                             |
| ----------------------- | ------ | --------------------------------------------------------------------------------------- |
| `_appTitle`             | string | A string append to every page title.                                                    |
| `_appName`              | string | The name of the site displayed after logo.                                              |
| `_appFooter`            | string | The footer HTML.                                                                        |
| `_appLogoPath`          | string | Path to the app logo.                                                                   |
| `_appLogoUrl`           | string | URL for the app logo.                                                                   |
| `_appFaviconPath`       | string | Favicon URL path.                                                                       |
| `_enableSearch`         | bool   | Whether to show the search box.                                                         |
| `_enableNewTab`         | bool   | Whether to open external links in a new tab.                                            |
| `_noindex`              | bool   | Whether to include in search results                                                    |
| `_disableContribution`  | bool   | Whether to show the _"Improve this Doc"_ and _"View Source"_ buttons.                   |
| `_gitContribute`        | object | Defines the `repo` and `branch` property of git links.                                  |
| `_gitUrlPattern`        | string | URL pattern of git links.                                                               |
| `_disableNavbar`        | bool   | Whether to show the navigation bar.                                                     |
| `_disableBreadcrumb`    | bool   | Whether to show the breadcrumb.                                                         |
| `_disableToc`           | bool   | Whether to show the TOC.                                                                |
| `_disableAffix`         | bool   | Whether to show the right rail.                                                         |
| `_googleAnalyticsTagId` | string | Enables Google Analytics web traffic analysis.                                          |
| `_lang`                 | string | Primary language of the page. If unset, the `<html>` tag will not have `lang` property. |

---

### Custom Template

Để xây dựng mẫu của riêng bạn, hãy tạo một thư mục mới và thêm nó vào `template` trong `docfx.json`:

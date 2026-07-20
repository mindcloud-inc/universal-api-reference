# Automatic Data Extraction: Native API Reference

A consolidated summary of Automatic Data Extraction's API configuration and 84 documented operations, with links to official documentation.

- **Official docs:** https://docs.zyte.com/zyte-api/usage/reference.html
- **API base URL:** `https://api.zyte.com/v1`

## Authentication

### Zyte API Basic Auth

Use your Zyte API key as the Basic Auth username and leave the password empty.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.zyte.com/zyte-api/usage/reference.html)

## Endpoints (84 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Extract Article](actions/extract-article.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Article From Browser HTML Only](actions/extract-article-from-browser-html-only.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Article From HTTP](actions/extract-article-from-http.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Article List](actions/extract-article-list.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Article List From Browser HTML Only](actions/extract-article-list-from-browser-html-only.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Article List From HTTP](actions/extract-article-list-from-http.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Article Navigation](actions/extract-article-navigation.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Article Navigation From Browser HTML Only](actions/extract-article-navigation-from-browser-html-only.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Article Navigation From HTTP](actions/extract-article-navigation-from-http.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Article With Custom Attributes](actions/extract-article-with-custom-attributes.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/extract/custom-attributes.html) |
| [Extract Article With Custom Attributes From Browser HTML Only](actions/extract-article-with-custom-attributes-from-browser-html-only.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/extract/custom-attributes.html) |
| [Extract Article With Custom Attributes From HTTP](actions/extract-article-with-custom-attributes-from-http.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/extract/custom-attributes.html) |
| [Extract Browser HTML](actions/extract-browser-html.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Browser HTML With Actions](actions/extract-browser-html-with-actions.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Browser HTML With Client Session](actions/extract-browser-html-with-client-session.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/features.html) |
| [Extract Browser HTML With Geolocation](actions/extract-browser-html-with-geolocation.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Browser HTML With Iframes](actions/extract-browser-html-with-iframes.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Browser HTML With JavaScript Disabled](actions/extract-browser-html-with-java-script-disabled.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Browser HTML With JavaScript Enabled](actions/extract-browser-html-with-java-script-enabled.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Browser HTML With Referer](actions/extract-browser-html-with-referer.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Browser HTML With Request Cookies](actions/extract-browser-html-with-request-cookies.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Browser HTML With Server Session Context](actions/extract-browser-html-with-server-session-context.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/features.html) |
| [Extract Browser HTML With Server Session Setup](actions/extract-browser-html-with-server-session-setup.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/features.html) |
| [Extract Browser HTML With Session Context](actions/extract-browser-html-with-session-context.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/features.html) |
| [Extract Browser HTML With Viewport](actions/extract-browser-html-with-viewport.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Forum Thread](actions/extract-forum-thread.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Forum Thread From Browser HTML Only](actions/extract-forum-thread-from-browser-html-only.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Forum Thread From HTTP](actions/extract-forum-thread-from-http.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Full Page Screenshot](actions/extract-full-page-screenshot.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract HTTP Body With Client Session](actions/extract-http-body-with-client-session.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/features.html) |
| [Extract HTTP Body With Cookie Management Discard](actions/extract-http-body-with-cookie-management-discard.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract HTTP Body With Datacenter IP](actions/extract-http-body-with-datacenter-ip.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/features.html) |
| [Extract HTTP Body With Echo Data](actions/extract-http-body-with-echo-data.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract HTTP Body With Geolocation](actions/extract-http-body-with-geolocation.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/features.html) |
| [Extract HTTP Body With Job ID](actions/extract-http-body-with-job-id.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract HTTP Body With Mobile Device](actions/extract-http-body-with-mobile-device.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract HTTP Body With Request Cookies](actions/extract-http-body-with-request-cookies.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract HTTP Body With Residential IP](actions/extract-http-body-with-residential-ip.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/features.html) |
| [Extract HTTP Body With Server Session Context](actions/extract-http-body-with-server-session-context.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/features.html) |
| [Extract HTTP Body With Server Session Setup](actions/extract-http-body-with-server-session-setup.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/features.html) |
| [Extract HTTP Body With Tags](actions/extract-http-body-with-tags.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract HTTP Body Without Redirect](actions/extract-http-body-without-redirect.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract HTTP Response Body](actions/extract-http-response-body.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract HTTP Response Body And Headers](actions/extract-http-response-body-and-headers.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract HTTP Response Headers](actions/extract-http-response-headers.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Job Posting](actions/extract-job-posting.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Job Posting From Browser HTML Only](actions/extract-job-posting-from-browser-html-only.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Job Posting From HTTP](actions/extract-job-posting-from-http.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Job Posting Navigation](actions/extract-job-posting-navigation.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Job Posting Navigation From Browser HTML Only](actions/extract-job-posting-navigation-from-browser-html-only.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Job Posting Navigation From HTTP](actions/extract-job-posting-navigation-from-http.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract JPEG Screenshot](actions/extract-jpeg-screenshot.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Network Capture](actions/extract-network-capture.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Page Content](actions/extract-page-content.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Page Content From Browser HTML Only](actions/extract-page-content-from-browser-html-only.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Page Content From HTTP](actions/extract-page-content-from-http.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract PNG Screenshot](actions/extract-png-screenshot.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Product](actions/extract-product.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Product From Browser HTML Only](actions/extract-product-from-browser-html-only.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Product From HTTP](actions/extract-product-from-http.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Product List](actions/extract-product-list.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Product List From Browser HTML Only](actions/extract-product-list-from-browser-html-only.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Product List From HTTP](actions/extract-product-list-from-http.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Product Model 2024-02-01](actions/extract-product-model20240201.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Product Model 2024-09-16](actions/extract-product-model20240916.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Product Navigation](actions/extract-product-navigation.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Product Navigation From Browser HTML Only](actions/extract-product-navigation-from-browser-html-only.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Product Navigation From HTTP](actions/extract-product-navigation-from-http.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Product With Custom Attributes](actions/extract-product-with-custom-attributes.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/extract/custom-attributes.html) |
| [Extract Product With Custom Attributes From Browser HTML Only](actions/extract-product-with-custom-attributes-from-browser-html-only.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/extract/custom-attributes.html) |
| [Extract Product With Custom Attributes From HTTP](actions/extract-product-with-custom-attributes-from-http.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/extract/custom-attributes.html) |
| [Extract Response Cookies](actions/extract-response-cookies.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Screenshot](actions/extract-screenshot.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract Screenshot With Actions](actions/extract-screenshot-with-actions.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract SERP](actions/extract-serp.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Extract SERP From Browser HTML](actions/extract-serp-from-browser-html.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Get Zyte API Stats](actions/get-zyte-api-stats.md) | `GET https://zyte-api-stats.zyte.com/api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Process Custom DELETE Request](actions/process-custom-delete-request.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Process Custom HEAD Request](actions/process-custom-head-request.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Process Custom HTTP Request](actions/process-custom-http-request.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Process Custom OPTIONS Request](actions/process-custom-options-request.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Process Custom PATCH Request](actions/process-custom-patch-request.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Process Custom POST Request](actions/process-custom-post-request.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |
| [Process Custom PUT Request](actions/process-custom-put-request.md) | `POST /extract` | [docs](https://docs.zyte.com/zyte-api/usage/reference.html) |

# <img src="https://images.mindcloud.co/apps/icons/zyte-icon-padded_1776260935936.png" alt="Automatic Data Extraction logo" width="28" height="28"> Automatic Data Extraction: Universal API

Extract structured web data, HTML, screenshots, and HTTP/browser responses from a single URL using Zyte API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/automaticDataExtraction/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 84
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zyte.com/zyte-api/
- **Vendor API docs:** https://docs.zyte.com/zyte-api/usage/reference.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Extract Browser HTML](actions/extract-browser-html.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/automaticDataExtraction/latest/actions/extract-browser-html?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (84)

### Article Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Article](actions/extract-article.md) | GET | Extracts article data in Automatic Data Extraction. |
| [Extract Article From HTTP](actions/extract-article-from-http.md) | GET | Extracts article data from HTTP in Automatic Data Extraction. |

### Article List Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Article List](actions/extract-article-list.md) | GET | Extracts article list data in Automatic Data Extraction. |
| [Extract Article List From HTTP](actions/extract-article-list-from-http.md) | GET | Extracts article list data from HTTP in Automatic Data Extraction. |

### Article Navigation Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Article Navigation](actions/extract-article-navigation.md) | GET | Extracts article navigation data in Automatic Data Extraction. |

### Extraction Result

| Action | Method | Description |
| --- | --- | --- |
| [Extract Article From Browser HTML Only](actions/extract-article-from-browser-html-only.md) | GET | Extracts article data from browser HTML only in Automatic Data Extraction. |
| [Extract Article List From Browser HTML Only](actions/extract-article-list-from-browser-html-only.md) | GET | Extracts article list data from browser HTML only in Automatic Data Extraction. |
| [Extract Article Navigation From Browser HTML Only](actions/extract-article-navigation-from-browser-html-only.md) | GET | Extracts article navigation data from browser HTML only in Automatic Data Extraction. |
| [Extract Article Navigation From HTTP](actions/extract-article-navigation-from-http.md) | GET | Extracts article navigation data from HTTP in Automatic Data Extraction. |
| [Extract Article With Custom Attributes](actions/extract-article-with-custom-attributes.md) | GET | Extracts article data and custom attributes in Automatic Data Extraction. |
| [Extract Article With Custom Attributes From Browser HTML Only](actions/extract-article-with-custom-attributes-from-browser-html-only.md) | GET | Extracts article custom attributes from browser HTML only in Automatic Data Extraction. |
| [Extract Article With Custom Attributes From HTTP](actions/extract-article-with-custom-attributes-from-http.md) | GET | Extracts article data and custom attributes from HTTP in Automatic Data Extraction. |
| [Extract Browser HTML](actions/extract-browser-html.md) | GET | Extracts browser HTML in Automatic Data Extraction. |
| [Extract Browser HTML With Actions](actions/extract-browser-html-with-actions.md) | GET | Extracts browser HTML after browser actions in Automatic Data Extraction. |
| [Extract Browser HTML With Client Session](actions/extract-browser-html-with-client-session.md) | GET | Extracts browser HTML with a client session in Automatic Data Extraction. |
| [Extract Browser HTML With Geolocation](actions/extract-browser-html-with-geolocation.md) | GET | Extracts browser HTML with geolocation in Automatic Data Extraction. |
| [Extract Browser HTML With Iframes](actions/extract-browser-html-with-iframes.md) | GET | Extracts browser HTML with iframes in Automatic Data Extraction. |
| [Extract Browser HTML With JavaScript Disabled](actions/extract-browser-html-with-java-script-disabled.md) | GET | Extracts browser HTML with JavaScript disabled in Automatic Data Extraction. |
| [Extract Browser HTML With JavaScript Enabled](actions/extract-browser-html-with-java-script-enabled.md) | GET | Extracts browser HTML with JavaScript enabled in Automatic Data Extraction. |
| [Extract Browser HTML With Referer](actions/extract-browser-html-with-referer.md) | GET | Extracts browser HTML with a referer in Automatic Data Extraction. |
| [Extract Browser HTML With Request Cookies](actions/extract-browser-html-with-request-cookies.md) | GET | Extracts browser HTML with request cookies in Automatic Data Extraction. |
| [Extract Browser HTML With Server Session Context](actions/extract-browser-html-with-server-session-context.md) | GET | Extracts browser HTML with server session context in Automatic Data Extraction. |
| [Extract Browser HTML With Server Session Setup](actions/extract-browser-html-with-server-session-setup.md) | GET | Extracts browser HTML with server session setup in Automatic Data Extraction. |
| [Extract Browser HTML With Session Context](actions/extract-browser-html-with-session-context.md) | GET | Extracts browser HTML with session context in Automatic Data Extraction. |
| [Extract Browser HTML With Viewport](actions/extract-browser-html-with-viewport.md) | GET | Extracts browser HTML with viewport settings in Automatic Data Extraction. |
| [Extract Forum Thread](actions/extract-forum-thread.md) | GET | Extracts forum thread data in Automatic Data Extraction. |
| [Extract Forum Thread From Browser HTML Only](actions/extract-forum-thread-from-browser-html-only.md) | GET | Extracts forum thread data from browser HTML only in Automatic Data Extraction. |
| [Extract Forum Thread From HTTP](actions/extract-forum-thread-from-http.md) | GET | Extracts forum thread data from HTTP in Automatic Data Extraction. |
| [Extract Full Page Screenshot](actions/extract-full-page-screenshot.md) | GET | Extracts a full-page screenshot in Automatic Data Extraction. |
| [Extract HTTP Body With Client Session](actions/extract-http-body-with-client-session.md) | GET | Extracts HTTP response body with a client session in Automatic Data Extraction. |
| [Extract HTTP Body With Cookie Management Discard](actions/extract-http-body-with-cookie-management-discard.md) | GET | Extracts HTTP response body while discarding cookie management in Automatic Data Extraction. |
| [Extract HTTP Body With Datacenter IP](actions/extract-http-body-with-datacenter-ip.md) | GET | Extracts HTTP response body with datacenter IPs in Automatic Data Extraction. |
| [Extract HTTP Body With Echo Data](actions/extract-http-body-with-echo-data.md) | GET | Extracts HTTP response body with echo data in Automatic Data Extraction. |
| [Extract HTTP Body With Geolocation](actions/extract-http-body-with-geolocation.md) | GET | Extracts HTTP response body with geolocation in Automatic Data Extraction. |
| [Extract HTTP Body With Job ID](actions/extract-http-body-with-job-id.md) | GET | Extracts HTTP response body with a job ID in Automatic Data Extraction. |
| [Extract HTTP Body With Mobile Device](actions/extract-http-body-with-mobile-device.md) | GET | Extracts HTTP response body with a mobile device in Automatic Data Extraction. |
| [Extract HTTP Body With Request Cookies](actions/extract-http-body-with-request-cookies.md) | GET | Extracts HTTP response body with request cookies in Automatic Data Extraction. |
| [Extract HTTP Body With Residential IP](actions/extract-http-body-with-residential-ip.md) | GET | Extracts HTTP response body with residential IPs in Automatic Data Extraction. |
| [Extract HTTP Body With Server Session Context](actions/extract-http-body-with-server-session-context.md) | GET | Extracts HTTP response body with server session context in Automatic Data Extraction. |
| [Extract HTTP Body With Server Session Setup](actions/extract-http-body-with-server-session-setup.md) | GET | Extracts HTTP response body with server session setup in Automatic Data Extraction. |
| [Extract HTTP Body With Tags](actions/extract-http-body-with-tags.md) | GET | Extracts HTTP response body with tags in Automatic Data Extraction. |
| [Extract HTTP Body Without Redirect](actions/extract-http-body-without-redirect.md) | GET | Extracts HTTP response body without redirects in Automatic Data Extraction. |
| [Extract HTTP Response Body](actions/extract-http-response-body.md) | GET | Extracts an HTTP response body in Automatic Data Extraction. |
| [Extract HTTP Response Body And Headers](actions/extract-http-response-body-and-headers.md) | GET | Extracts HTTP response body and headers in Automatic Data Extraction. |
| [Extract HTTP Response Headers](actions/extract-http-response-headers.md) | GET | Extracts HTTP response headers in Automatic Data Extraction. |
| [Extract Job Posting](actions/extract-job-posting.md) | GET | Extracts job posting data in Automatic Data Extraction. |
| [Extract Job Posting From Browser HTML Only](actions/extract-job-posting-from-browser-html-only.md) | GET | Extracts job posting data from browser HTML only in Automatic Data Extraction. |
| [Extract Job Posting From HTTP](actions/extract-job-posting-from-http.md) | GET | Extracts job posting data from HTTP in Automatic Data Extraction. |
| [Extract Job Posting Navigation](actions/extract-job-posting-navigation.md) | GET | Extracts job posting navigation data in Automatic Data Extraction. |
| [Extract Job Posting Navigation From Browser HTML Only](actions/extract-job-posting-navigation-from-browser-html-only.md) | GET | Extracts job posting navigation data from browser HTML only in Automatic Data Extraction. |
| [Extract Job Posting Navigation From HTTP](actions/extract-job-posting-navigation-from-http.md) | GET | Extracts job posting navigation data from HTTP in Automatic Data Extraction. |
| [Extract JPEG Screenshot](actions/extract-jpeg-screenshot.md) | GET | Extracts a JPEG screenshot in Automatic Data Extraction. |
| [Extract Network Capture](actions/extract-network-capture.md) | GET | Extracts network capture data in Automatic Data Extraction. |
| [Extract Page Content](actions/extract-page-content.md) | GET | Extracts page content in Automatic Data Extraction. |
| [Extract Page Content From Browser HTML Only](actions/extract-page-content-from-browser-html-only.md) | GET | Extracts page content from browser HTML only in Automatic Data Extraction. |
| [Extract Page Content From HTTP](actions/extract-page-content-from-http.md) | GET | Extracts page content from HTTP in Automatic Data Extraction. |
| [Extract PNG Screenshot](actions/extract-png-screenshot.md) | GET | Extracts a PNG screenshot in Automatic Data Extraction. |
| [Extract Product](actions/extract-product.md) | GET | Extracts product data in Automatic Data Extraction. |
| [Extract Product From Browser HTML Only](actions/extract-product-from-browser-html-only.md) | GET | Extracts product data from browser HTML only in Automatic Data Extraction. |
| [Extract Product From HTTP](actions/extract-product-from-http.md) | GET | Extracts product data from HTTP in Automatic Data Extraction. |
| [Extract Product List](actions/extract-product-list.md) | GET | Extracts product list data in Automatic Data Extraction. |
| [Extract Product List From Browser HTML Only](actions/extract-product-list-from-browser-html-only.md) | GET | Extracts product list data from browser HTML only in Automatic Data Extraction. |
| [Extract Product List From HTTP](actions/extract-product-list-from-http.md) | GET | Extracts product list data from HTTP in Automatic Data Extraction. |
| [Extract Product Model 2024-02-01](actions/extract-product-model20240201.md) | GET | Extracts product data with the 2024-02-01 model in Automatic Data Extraction. |
| [Extract Product Model 2024-09-16](actions/extract-product-model20240916.md) | GET | Extracts product data with the 2024-09-16 model in Automatic Data Extraction. |
| [Extract Product Navigation](actions/extract-product-navigation.md) | GET | Extracts product navigation data in Automatic Data Extraction. |
| [Extract Product Navigation From Browser HTML Only](actions/extract-product-navigation-from-browser-html-only.md) | GET | Extracts product navigation data from browser HTML only in Automatic Data Extraction. |
| [Extract Product Navigation From HTTP](actions/extract-product-navigation-from-http.md) | GET | Extracts product navigation data from HTTP in Automatic Data Extraction. |
| [Extract Product With Custom Attributes](actions/extract-product-with-custom-attributes.md) | GET | Extracts product data and custom attributes in Automatic Data Extraction. |
| [Extract Product With Custom Attributes From Browser HTML Only](actions/extract-product-with-custom-attributes-from-browser-html-only.md) | GET | Extracts product custom attributes from browser HTML only in Automatic Data Extraction. |
| [Extract Product With Custom Attributes From HTTP](actions/extract-product-with-custom-attributes-from-http.md) | GET | Extracts product data and custom attributes from HTTP in Automatic Data Extraction. |
| [Extract Response Cookies](actions/extract-response-cookies.md) | GET | Extracts response cookies in Automatic Data Extraction. |
| [Extract Screenshot](actions/extract-screenshot.md) | GET | Extracts a screenshot in Automatic Data Extraction. |
| [Extract Screenshot With Actions](actions/extract-screenshot-with-actions.md) | GET | Extracts a screenshot after browser actions in Automatic Data Extraction. |
| [Extract SERP](actions/extract-serp.md) | GET | Extracts SERP data in Automatic Data Extraction. |
| [Extract SERP From Browser HTML](actions/extract-serp-from-browser-html.md) | GET | Extracts SERP data from browser HTML in Automatic Data Extraction. |
| [Process Custom DELETE Request](actions/process-custom-delete-request.md) | GET | Processes a custom DELETE request in Automatic Data Extraction. |
| [Process Custom HEAD Request](actions/process-custom-head-request.md) | GET | Processes a custom HEAD request in Automatic Data Extraction. |
| [Process Custom HTTP Request](actions/process-custom-http-request.md) | GET | Processes a custom HTTP request in Automatic Data Extraction. |
| [Process Custom OPTIONS Request](actions/process-custom-options-request.md) | GET | Processes a custom OPTIONS request in Automatic Data Extraction. |
| [Process Custom PATCH Request](actions/process-custom-patch-request.md) | GET | Processes a custom PATCH request in Automatic Data Extraction. |
| [Process Custom POST Request](actions/process-custom-post-request.md) | GET | Processes a custom POST request in Automatic Data Extraction. |
| [Process Custom PUT Request](actions/process-custom-put-request.md) | GET | Processes a custom PUT request in Automatic Data Extraction. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Zyte API Stats](actions/get-zyte-api-stats.md) | GET | Retrieves Zyte API usage stats from Automatic Data Extraction. |


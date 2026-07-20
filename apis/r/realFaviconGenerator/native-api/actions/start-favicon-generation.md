# Start favicon generation with RealFaviconGenerator

## Endpoint

- **Method:** `GET`
- **Path:** `/favicon_generator`
- **Base URL:** `https://realfavicongenerator.net/api`
- **Official documentation:** [Start favicon generation](https://realfavicongenerator.net/developers/favicon-generation/interactive-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `master_picture.type` | query | `list` | no | How the master favicon picture is supplied: no picture, URL, or inline Base64 content. Accepted values: `inline`, `no_picture`, `url`. |
| `master_picture.url` | query | `string` | no | URL of the source image when Master picture type is url. |
| `master_picture.content` | query | `string` | no | Base64-encoded image content when Master picture type is inline. |
| `master_picture.demo` | query | `boolean` | no | When no master picture is supplied, show RealFaviconGenerator's demo option. |
| `files_location.type` | query | `list` | no | How the favicon file deployment location is chosen. Accepted values: `no_location`, `path`, `root`. |
| `files_location.path` | query | `string` | no | Deployment path when Files location type is path, such as /assets/icons. |
| `callback.type` | query | `list` | no | Whether RealFaviconGenerator redirects to a callback URL or lets the user download directly. Accepted values: `none`, `url`. |
| `callback.url` | query | `string` | no | URL RealFaviconGenerator redirects to after generation when Callback type is url. |
| `callback.short_url` | query | `boolean` | no | Return a json_result_url callback instead of embedding the JSON result in the callback URL. |
| `callback.path_only` | query | `boolean` | no | When short callback URLs are enabled, return only a path so the receiver can prepend the RealFaviconGenerator host. |
| `callback.custom_parameter` | query | `string` | no | Custom query-string fragment returned to the callback URL, such as ref=157539001. |

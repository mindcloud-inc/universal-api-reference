# TinyPNG: Native API Reference

A consolidated summary of TinyPNG's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://tinify.com/developers/reference/http
- **API base URL:** `https://api.tinify.com`

## Authentication

### Basic Auth

HTTP Basic auth for the Tinify API using username `api` and the tenant API key as the password.

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

[Official authentication documentation](https://tinify.com/developers/reference/http)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compress Image From URL](actions/compress-image-from-url.md) | `POST /shrink` | [docs](https://tinify.com/developers/reference/http#compressing-images) |
| [Convert Image To AVIF](actions/convert-image-to-avif.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#converting-images) |
| [Convert Image To JPEG Black Background](actions/convert-image-to-jpeg-black-background.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#converting-images) |
| [Convert Image To JPEG White Background](actions/convert-image-to-jpeg-white-background.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#converting-images) |
| [Convert Image To PNG](actions/convert-image-to-png.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#converting-images) |
| [Convert Image To Smallest Supported Format](actions/convert-image-to-smallest-supported-format.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#converting-images) |
| [Convert Image To WebP](actions/convert-image-to-web-p.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#converting-images) |
| [Download Optimized Image](actions/download-optimized-image.md) | `GET {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#compressing-images) |
| [Preserve Copyright And Creation Metadata](actions/preserve-copyright-and-creation-metadata.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#preserving-metadata) |
| [Preserve Copyright Metadata](actions/preserve-copyright-metadata.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#preserving-metadata) |
| [Preserve Creation Metadata](actions/preserve-creation-metadata.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#preserving-metadata) |
| [Preserve Location Metadata](actions/preserve-location-metadata.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#preserving-metadata) |
| [Resize Image Cover Custom](actions/resize-image-cover-custom.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Cover 300x300](actions/resize-image-cover300x300.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Fit Custom](actions/resize-image-fit-custom.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Fit 150x100](actions/resize-image-fit150x100.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Fit 300x200](actions/resize-image-fit300x200.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Scale Custom](actions/resize-image-scale-custom.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Scale To Height 150](actions/resize-image-scale-to-height150.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Scale To Height 300](actions/resize-image-scale-to-height300.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Scale To Height 600](actions/resize-image-scale-to-height600.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Scale To Height 64](actions/resize-image-scale-to-height64.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Scale To Width 150](actions/resize-image-scale-to-width150.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Scale To Width 300](actions/resize-image-scale-to-width300.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Scale To Width 600](actions/resize-image-scale-to-width600.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Scale To Width 64](actions/resize-image-scale-to-width64.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Thumb Custom](actions/resize-image-thumb-custom.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Resize Image Thumb 150x150](actions/resize-image-thumb150x150.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Store Image To Amazon S3](actions/store-image-to-amazon-s3.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#saving-to-amazon-s3) |
| [Store Image To Google Cloud Storage](actions/store-image-to-google-cloud-storage.md) | `POST {{outputPath}}` | [docs](https://tinify.com/developers/reference/http#saving-to-google-cloud-storage) |

# Google Cloud Storage: Native API Reference

A consolidated summary of Google Cloud Storage's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://docs.cloud.google.com/storage/docs/json_api
- **API base URL:** `https://storage.googleapis.com`

## Authentication

### OAuth 2.0

### Credentials

- **Project ID:** `project` · required · The Google Cloud Project ID that contains the Cloud Storage bucket you want to use. You can find it in Google Cloud Console from the project selector at the top of the page.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/devstorage.read_write`.

Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/web-server)

### Service Account

Authenticate Google Cloud Storage with a Google Cloud service account private key.

### Credentials

- **Project ID:** `project` · required · The Google Cloud project ID that contains the Cloud Storage buckets this connection should access.
- **Client Email:** `clientEmail` · required · The client_email value from the service account key JSON file.
- **Private Key:** `privateKeySecret` · required · The private_key value from the service account key JSON file. MindCloud uses it only to sign short-lived Google OAuth JWT assertions.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/service-account)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `maxResults` in the query string to set the page size (default 25; accepted range 1–1000). Use `pageToken` in the query string as the pagination cursor.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compose Object](actions/compose-object.md) | `POST /storage/v1/b/:destinationBucket/o/:destinationObject/compose` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/compose) |
| [Copy Object](actions/copy-object.md) | `POST /storage/v1/b/:sourceBucket/o/:sourceObject/copyTo/b/:destinationBucket/o/:destinationObject` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/copy) |
| [Create Bucket](actions/create-bucket.md) | `POST /storage/v1/b` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/buckets/insert) |
| [Get Bucket](actions/get-bucket.md) | `GET /storage/v1/b/:bucket` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/buckets/get) |
| [Get Bucket Storage Layout](actions/get-bucket-storage-layout.md) | `GET /storage/v1/b/:bucket/storageLayout` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/buckets/getStorageLayout) |
| [Get Object Metadata](actions/get-object-metadata.md) | `GET /storage/v1/b/:bucket/o/:object` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/get) |
| [List Buckets](actions/list-buckets.md) | `GET /storage/v1/b` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/buckets/list) |
| [List Objects](actions/list-objects.md) | `GET /storage/v1/b/:bucket/o` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/list) |
| [Move Object](actions/move-object.md) | `POST /storage/v1/b/:bucket/o/:sourceObject/moveTo/o/:destinationObject` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/move) |
| [Restore Object](actions/restore-object.md) | `POST /storage/v1/b/:bucket/o/:object/restore` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/restore) |
| [Rewrite Object](actions/rewrite-object.md) | `POST /storage/v1/b/:sourceBucket/o/:sourceObject/rewriteTo/b/:destinationBucket/o/:destinationObject` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/rewrite) |
| [Update Bucket](actions/update-bucket.md) | `PATCH /storage/v1/b/:bucket` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/buckets/patch) |
| [Update Object Metadata](actions/update-object-metadata.md) | `PATCH /storage/v1/b/:bucket/o/:object` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/patch) |
| [Upload Object](actions/upload-object.md) | `POST /upload/storage/v1/b/:bucket/o` | [docs](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/insert) |

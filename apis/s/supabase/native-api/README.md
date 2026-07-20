# Supabase: Native API Reference

A consolidated summary of Supabase's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://supabase.com/docs/reference/javascript
- **API base URL:** `{projectUrl}`

## Authentication

### Server API Key

Use a Supabase project URL and server-side project key for elevated project API access.

### Credentials

- **API Key:** `apiKey` · required
- **Project URL:** `projectUrl` · required · Supabase project URL, for example https://your-project.supabase.co

Send these headers with each API request:

```http
apikey: <apiKey>
authorization: Bearer <apiKey>
```

[Official authentication documentation](https://supabase.com/docs/guides/api/api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy Object](actions/copy-object.md) | `POST /storage/v1/object/copy` | [docs](https://supabase.com/docs/reference/javascript/storage-from-copy) |
| [Create Bucket](actions/create-bucket.md) | `POST /storage/v1/bucket` | [docs](https://supabase.com/docs/reference/javascript/storage-createbucket) |
| [Create Signed Download URL](actions/create-signed-download-url.md) | `POST /storage/v1/object/sign/:bucketName/:objectPath` | [docs](https://supabase.com/docs/reference/javascript/storage-from-createsignedurl) |
| [Create Signed Download URLs](actions/create-signed-download-urls.md) | `POST /storage/v1/object/sign/:bucketName` | [docs](https://supabase.com/docs/reference/javascript/storage-from-createsignedurls) |
| [Create Signed Upload URL](actions/create-signed-upload-url.md) | `POST /storage/v1/object/upload/sign/:bucketName/:objectPath` | [docs](https://supabase.com/docs/reference/javascript/storage-from-createsigneduploadurl) |
| [Delete Bucket](actions/delete-bucket.md) | `DELETE /storage/v1/bucket/:bucketId` | [docs](https://supabase.com/docs/reference/javascript/storage-deletebucket) |
| [Delete Object](actions/delete-object.md) | `DELETE /storage/v1/object/:bucketName/:objectPath` | [docs](https://supabase.com/docs/reference/javascript/storage-from-remove) |
| [Delete Objects](actions/delete-objects.md) | `DELETE /storage/v1/object/:bucketName` | [docs](https://supabase.com/docs/reference/javascript/storage-from-remove) |
| [Delete Rows](actions/delete-rows.md) | `DELETE /rest/v1/:table` | [docs](https://supabase.com/docs/reference/javascript/delete) |
| [Delete User](actions/delete-user.md) | `DELETE /auth/v1/admin/users/:userId` | [docs](https://supabase.com/docs/reference/javascript/auth-admin-deleteuser) |
| [Delete User MFA Factor](actions/delete-user-mfa-factor.md) | `DELETE /auth/v1/admin/users/:userId/factors/:factorId` | [docs](https://supabase.com/docs/reference/javascript/auth-admin-mfa-deletefactor) |
| [Empty Bucket](actions/empty-bucket.md) | `POST /storage/v1/bucket/:bucketId/empty` | [docs](https://supabase.com/docs/reference/javascript/storage-emptybucket) |
| [Generate Email Link](actions/generate-email-link.md) | `POST /auth/v1/admin/generate_link` | [docs](https://supabase.com/docs/reference/javascript/auth-admin-generatelink) |
| [Get Bucket](actions/get-bucket.md) | `GET /storage/v1/bucket/:bucketId` | [docs](https://supabase.com/docs/reference/javascript/storage-getbucket) |
| [Get Object](actions/get-object.md) | `GET /storage/v1/object/:bucketName/:objectPath` | [docs](https://supabase.com/docs/reference/javascript/storage-from-download) |
| [Get Object Info](actions/get-object-info.md) | `GET /storage/v1/object/info/:bucketName/:objectPath` | [docs](https://supabase.com/docs/reference/javascript/storage-from-info) |
| [Get Public Object](actions/get-public-object.md) | `GET /storage/v1/object/public/:bucketName/:objectPath` | [docs](https://supabase.com/docs/reference/javascript/storage-from-getpublicurl) |
| [Get Single Row](actions/get-single-row.md) | `GET /rest/v1/:table` | [docs](https://supabase.com/docs/reference/javascript/select) |
| [Get User](actions/get-user.md) | `GET /auth/v1/admin/users/:userId` | [docs](https://supabase.com/docs/reference/javascript/auth-admin-getuserbyid) |
| [Insert Row](actions/insert-row.md) | `POST /rest/v1/:table` | [docs](https://supabase.com/docs/reference/javascript/insert) |
| [Insert Rows (Bulk)](actions/insert-rows-bulk.md) | `POST /rest/v1/:table` | [docs](https://supabase.com/docs/reference/javascript/insert) |
| [Invite User](actions/invite-user.md) | `POST /auth/v1/invite` | [docs](https://supabase.com/docs/reference/javascript/auth-admin-inviteuserbyemail) |
| [Invoke RPC (Read)](actions/invoke-rpc-read.md) | `GET /rest/v1/rpc/:functionName` | [docs](https://supabase.com/docs/reference/javascript/rpc) |
| [Invoke RPC (Write)](actions/invoke-rpc-write.md) | `POST /rest/v1/rpc/:functionName` | [docs](https://supabase.com/docs/reference/javascript/rpc) |
| [List Audit Logs](actions/list-audit-logs.md) | `GET /auth/v1/admin/audit` | [docs](https://supabase.com/docs/reference/javascript/admin-api) |
| [List Buckets](actions/list-buckets.md) | `GET /storage/v1/bucket` | [docs](https://supabase.com/docs/reference/javascript/storage-listbuckets) |
| [List Objects](actions/list-objects.md) | `POST /storage/v1/object/list-v2/:bucketName` | [docs](https://supabase.com/docs/reference/javascript/storage-from-list) |
| [List Rows](actions/list-rows.md) | `GET /rest/v1/:table` | [docs](https://supabase.com/docs/reference/javascript/select) |
| [List User MFA Factors](actions/list-user-mfa-factors.md) | `GET /auth/v1/admin/users/:userId/factors` | [docs](https://supabase.com/docs/reference/javascript/auth-admin-mfa-listfactors-admin) |
| [List Users](actions/list-users.md) | `GET /auth/v1/admin/users` | [docs](https://supabase.com/docs/reference/javascript/auth-admin-listusers) |
| [Move Object](actions/move-object.md) | `POST /storage/v1/object/move` | [docs](https://supabase.com/docs/reference/javascript/storage-from-move) |
| [Update Bucket](actions/update-bucket.md) | `PUT /storage/v1/bucket/:bucketId` | [docs](https://supabase.com/docs/reference/javascript/storage-updatebucket) |
| [Update Object](actions/update-object.md) | `PUT /storage/v1/object/:bucketName/:objectPath` | [docs](https://supabase.com/docs/reference/javascript/storage-from-update) |
| [Update Rows](actions/update-rows.md) | `PATCH /rest/v1/:table` | [docs](https://supabase.com/docs/reference/javascript/update) |
| [Update User](actions/update-user.md) | `PUT /auth/v1/admin/users/:userId` | [docs](https://supabase.com/docs/reference/javascript/auth-admin-updateuserbyid) |
| [Update User MFA Factor](actions/update-user-mfa-factor.md) | `PUT /auth/v1/admin/users/:userId/factors/:factorId` | [docs](https://supabase.com/docs/reference/javascript/admin-api) |
| [Upload Object](actions/upload-object.md) | `POST /storage/v1/object/:bucketName/:objectPath` | [docs](https://supabase.com/docs/reference/javascript/storage-from-upload) |
| [Upload Via Signed URL](actions/upload-via-signed-url.md) | `PUT /storage/v1/object/upload/sign/:bucketName/:objectPath` | [docs](https://supabase.com/docs/reference/javascript/storage-from-uploadtosignedurl) |
| [Upsert Rows](actions/upsert-rows.md) | `POST /rest/v1/:table` | [docs](https://supabase.com/docs/reference/javascript/upsert) |

# <img src="https://images.mindcloud.co/apps/icons/supabase_1775584402527.png" alt="Supabase logo" width="28" height="28"> Supabase: Universal API

Supabase: Query Postgres data, manage auth users, and manage storage buckets and objects.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/supabase/latest
- **Category:** IT Operations / Database
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://supabase.com
- **Vendor API docs:** https://supabase.com/docs/reference/javascript

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Buckets](actions/list-buckets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-buckets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [List Audit Logs](actions/list-audit-logs.md) | GET |  |

### Auth Link

| Action | Method | Description |
| --- | --- | --- |
| [Generate Email Link](actions/generate-email-link.md) | POST | Generates a Supabase Auth email action link. |

### Bucket

| Action | Method | Description |
| --- | --- | --- |
| [Create Bucket](actions/create-bucket.md) | POST | Creates a storage bucket in your Supabase project. |
| [Delete Bucket](actions/delete-bucket.md) | DELETE | Deletes a storage bucket from your Supabase project. |
| [Empty Bucket](actions/empty-bucket.md) | PUT | Deletes all objects from a Supabase storage bucket. |
| [Get Bucket](actions/get-bucket.md) | GET | Retrieves a storage bucket from your Supabase project. |
| [List Buckets](actions/list-buckets.md) | GET | Retrieves storage buckets from your Supabase project. |
| [Update Bucket](actions/update-bucket.md) | PUT | Updates a storage bucket in your Supabase project. |

### Mfa Factor

| Action | Method | Description |
| --- | --- | --- |
| [Delete User MFA Factor](actions/delete-user-mfa-factor.md) | DELETE | Deletes a user's MFA factor from Supabase Auth. |
| [List User MFA Factors](actions/list-user-mfa-factors.md) | GET | Retrieves a user's MFA factors from Supabase Auth. |
| [Update User MFA Factor](actions/update-user-mfa-factor.md) | PUT |  |

### Object

| Action | Method | Description |
| --- | --- | --- |
| [Copy Object](actions/copy-object.md) | POST | Copies an object between paths in Supabase storage. |
| [Delete Object](actions/delete-object.md) | DELETE | Deletes an object from a Supabase storage bucket. |
| [Delete Objects](actions/delete-objects.md) | DELETE | Deletes multiple objects from a Supabase storage bucket. |
| [Get Object](actions/get-object.md) | GET | Retrieves an object from a Supabase storage bucket. |
| [Get Object Info](actions/get-object-info.md) | GET | Retrieves object details from a Supabase storage bucket. |
| [Get Public Object](actions/get-public-object.md) | GET | Retrieves the public URL for a Supabase object. |
| [List Objects](actions/list-objects.md) | GET | Retrieves objects from a Supabase storage bucket. |
| [Move Object](actions/move-object.md) | PUT | Moves an object between paths in Supabase storage. |
| [Update Object](actions/update-object.md) | PUT | Replaces an object in a Supabase storage bucket. |
| [Upload Object](actions/upload-object.md) | POST | Uploads an object to a Supabase storage bucket. |
| [Upload Via Signed URL](actions/upload-via-signed-url.md) | PUT | Uploads an object to Supabase using a signed URL. |

### Row

| Action | Method | Description |
| --- | --- | --- |
| [Delete Rows](actions/delete-rows.md) | DELETE | Deletes rows from a Supabase table. |
| [Get Single Row](actions/get-single-row.md) | GET | Retrieves a single row from a Supabase table. |
| [Insert Row](actions/insert-row.md) | POST | Creates a row in a Supabase table. |
| [Insert Rows (Bulk)](actions/insert-rows-bulk.md) | POST | Creates multiple rows in a Supabase table. |
| [List Rows](actions/list-rows.md) | GET | Retrieves rows from a table in Supabase. |
| [Update Rows](actions/update-rows.md) | PUT | Updates rows in a Supabase table. |
| [Upsert Rows](actions/upsert-rows.md) | PUT | Creates or updates rows in a Supabase table. |

### Rpc Function

| Action | Method | Description |
| --- | --- | --- |
| [Invoke RPC (Read)](actions/invoke-rpc-read.md) | GET | Invokes a read-only RPC function in Supabase. |
| [Invoke RPC (Write)](actions/invoke-rpc-write.md) | PUT | Invokes a mutating RPC function in Supabase. |

### Signed Upload Url

| Action | Method | Description |
| --- | --- | --- |
| [Create Signed Upload URL](actions/create-signed-upload-url.md) | POST | Creates a signed upload URL for a Supabase object. |

### Signed Url

| Action | Method | Description |
| --- | --- | --- |
| [Create Signed Download URL](actions/create-signed-download-url.md) | POST | Creates a signed download URL for a Supabase object. |
| [Create Signed Download URLs](actions/create-signed-download-urls.md) | POST | Creates signed download URLs for Supabase objects. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from Supabase Auth. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Supabase Auth. |
| [Invite User](actions/invite-user.md) | POST | Invites a user to Supabase Auth by email. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Supabase Auth administration. |
| [Update User](actions/update-user.md) | PUT | Updates a user in Supabase Auth. |


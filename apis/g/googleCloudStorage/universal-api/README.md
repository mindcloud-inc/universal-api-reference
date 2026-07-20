# <img src="https://images.mindcloud.co/apps/icons/b9c95a69-55ff-4799-947f-ad209da7df67_1776183589710.png" alt="Google Cloud Storage logo" width="28" height="28"> Google Cloud Storage: Universal API

Google Cloud Storage through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleCloudStorage/latest
- **Category:** Content & Files / Storage
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloud.google.com/storage
- **Vendor API docs:** https://docs.cloud.google.com/storage/docs/json_api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Buckets](actions/list-buckets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/list-buckets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Compose Object](actions/compose-object.md) | POST | Composes multiple objects into one in Google Cloud Storage. |
| [Copy Object](actions/copy-object.md) | POST | Copies an object to a destination in Google Cloud Storage. |
| [Get Object Metadata](actions/get-object-metadata.md) | GET | Retrieves object metadata from Google Cloud Storage. |
| [List Objects](actions/list-objects.md) | GET | Retrieves a list of objects from Google Cloud Storage. |
| [Move Object](actions/move-object.md) | PUT | Moves an object within a bucket in Google Cloud Storage. |
| [Restore Object](actions/restore-object.md) | POST | Restores a soft-deleted object in Google Cloud Storage. |
| [Rewrite Object](actions/rewrite-object.md) | PUT | Rewrites an object to a destination in Google Cloud Storage. |
| [Update Object Metadata](actions/update-object-metadata.md) | PUT | Updates object metadata in Google Cloud Storage. |
| [Upload Object](actions/upload-object.md) | POST | Uploads an object to Google Cloud Storage. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Bucket](actions/create-bucket.md) | POST | Creates a new bucket in Google Cloud Storage. |
| [Get Bucket](actions/get-bucket.md) | GET | Retrieves bucket metadata from Google Cloud Storage. |
| [Get Bucket Storage Layout](actions/get-bucket-storage-layout.md) | GET | Retrieves a bucket's storage layout from Google Cloud Storage. |
| [List Buckets](actions/list-buckets.md) | GET | Retrieves a list of buckets from Google Cloud Storage. |
| [Update Bucket](actions/update-bucket.md) | PUT | Updates an existing bucket in Google Cloud Storage. |


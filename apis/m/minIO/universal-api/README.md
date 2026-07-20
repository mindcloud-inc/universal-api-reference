# <img src="https://images.mindcloud.co/apps/icons/min-io_1776187419465.png" alt="MinIO logo" width="28" height="28"> MinIO: Universal API

S3-compatible object storage for buckets and objects backed by MinIO AIStor and MinIO-compatible deployments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/minIO/latest
- **Category:** Content & Files / Storage
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://min.io/
- **Vendor API docs:** https://docs.min.io/community/minio-object-store/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Buckets](actions/list-buckets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minIO/latest/actions/list-buckets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Copy Object](actions/copy-object.md) | POST |  |
| [Delete Object](actions/delete-object.md) | DELETE |  |
| [Delete Object Tagging](actions/delete-object-tagging.md) | DELETE |  |
| [Delete Objects](actions/delete-objects.md) | DELETE |  |
| [Get Object](actions/get-object.md) | GET |  |
| [Get Object Attributes](actions/get-object-attributes.md) | GET |  |
| [Get Object Tagging](actions/get-object-tagging.md) | GET |  |
| [List Object Versions](actions/list-object-versions.md) | GET |  |
| [List Objects](actions/list-objects.md) | GET |  |
| [List Objects V2](actions/list-objects-v2.md) | GET |  |
| [Put Object](actions/put-object.md) | POST |  |
| [Put Object Tagging](actions/put-object-tagging.md) | PUT |  |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Bucket](actions/create-bucket.md) | POST |  |
| [Delete Bucket](actions/delete-bucket.md) | DELETE |  |
| [Delete Bucket CORS](actions/delete-bucket-cors.md) | DELETE |  |
| [Delete Bucket Lifecycle](actions/delete-bucket-lifecycle.md) | DELETE |  |
| [Delete Bucket Policy](actions/delete-bucket-policy.md) | DELETE |  |
| [Delete Bucket Tagging](actions/delete-bucket-tagging.md) | DELETE |  |
| [Get Bucket Encryption](actions/get-bucket-encryption.md) | GET |  |
| [Get Bucket Lifecycle Configuration](actions/get-bucket-lifecycle-configuration.md) | GET |  |
| [Get Bucket Location](actions/get-bucket-location.md) | GET |  |
| [Get Bucket Policy](actions/get-bucket-policy.md) | GET |  |
| [Get Bucket Tagging](actions/get-bucket-tagging.md) | GET |  |
| [Get Bucket Versioning](actions/get-bucket-versioning.md) | GET |  |
| [List Buckets](actions/list-buckets.md) | GET |  |
| [Put Bucket CORS](actions/put-bucket-cors.md) | PUT |  |
| [Put Bucket Lifecycle Configuration](actions/put-bucket-lifecycle-configuration.md) | PUT |  |
| [Put Bucket Policy](actions/put-bucket-policy.md) | PUT |  |
| [Put Bucket Tagging](actions/put-bucket-tagging.md) | PUT |  |
| [Put Bucket Versioning](actions/put-bucket-versioning.md) | PUT |  |


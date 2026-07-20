# <img src="https://images.mindcloud.co/apps/icons/backendless_1775050669662.png" alt="Backendless logo" width="28" height="28"> Backendless: Universal API

Backendless is a backend-as-a-service platform for user management, data storage, file storage, caching, and atomic counters.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/backendless/latest
- **Category:** IT Operations / Database
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://backendless.com
- **Vendor API docs:** https://backendless.com/docs/rest/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Root Directory](actions/list-root-directory.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/backendless/latest/actions/list-root-directory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Cache

| Action | Method | Description |
| --- | --- | --- |
| [Check Cache Key](actions/check-cache-key.md) | GET | Checks whether a cache key exists in Backendless. |
| [Delete Cache Value](actions/delete-cache-value.md) | DELETE | Deletes an existing cache value from Backendless. |
| [Extend Cache TTL](actions/extend-cache-ttl.md) | PUT | Extends a cache value TTL in Backendless. |
| [Get Cache Value](actions/get-cache-value.md) | GET | Retrieves a cache value from Backendless. |
| [Put Cache Value](actions/put-cache-value.md) | POST | Stores a cache value in Backendless. |

### Counters

| Action | Method | Description |
| --- | --- | --- |
| [Compare And Set Counter](actions/compare-and-set-counter.md) | PUT | Updates a counter conditionally in Backendless. |
| [Decrement Counter](actions/decrement-counter.md) | PUT | Decrements a counter in Backendless. |
| [Get Counter Value](actions/get-counter-value.md) | GET | Retrieves a counter value from Backendless. |
| [Increment Counter](actions/increment-counter.md) | PUT | Increments a counter in Backendless. |
| [List Counters](actions/list-counters.md) | GET | Retrieves counters from Backendless by name pattern. |

### Data

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Data Objects](actions/bulk-create-data-objects.md) | POST | Creates multiple data objects in Backendless. |
| [Bulk Delete Data Objects](actions/bulk-delete-data-objects.md) | DELETE | Deletes multiple data objects from Backendless. |
| [Bulk Update Data Objects](actions/bulk-update-data-objects.md) | PUT | Updates multiple data objects in Backendless. |
| [Count Data Objects](actions/count-data-objects.md) | GET | Retrieves a data object count from Backendless. |
| [Create Data Object](actions/create-data-object.md) | POST | Creates a new data object in Backendless. |
| [Delete Data Object](actions/delete-data-object.md) | DELETE | Deletes an existing data object from Backendless. |
| [Get Data Object](actions/get-data-object.md) | GET | Retrieves a data object from Backendless. |
| [Get First Data Object](actions/get-first-data-object.md) | GET | Retrieves the first data object from Backendless. |
| [Get Last Data Object](actions/get-last-data-object.md) | GET | Retrieves the last data object from Backendless. |
| [List Data Objects](actions/list-data-objects.md) | GET | Retrieves data objects from Backendless. |
| [Update Data Object](actions/update-data-object.md) | PUT | Updates an existing data object in Backendless. |
| [Upsert Data Object](actions/upsert-data-object.md) | PUT | Creates or updates a data object in Backendless. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Append File](actions/append-file.md) | PUT | Appends content to a file in Backendless. |
| [Copy File Or Folder](actions/copy-file-or-folder.md) | POST | Copies a file or folder in Backendless. |
| [Count Directory Items](actions/count-directory-items.md) | GET | Retrieves the item count for a Backendless directory. |
| [Create Directory](actions/create-directory.md) | POST | Creates a new directory in Backendless. |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from Backendless. |
| [List Directory](actions/list-directory.md) | GET | Retrieves a directory listing from Backendless. |
| [List Root Directory](actions/list-root-directory.md) | GET | Retrieves the root directory listing from Backendless. |
| [Move File Or Folder](actions/move-file-or-folder.md) | PUT | Moves a file or folder in Backendless. |
| [Rename File Or Folder](actions/rename-file-or-folder.md) | PUT | Renames a file or folder in Backendless. |
| [Save Binary File](actions/save-binary-file.md) | POST | Saves a binary file to Backendless. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Backendless. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Login User](actions/login-user.md) | GET | Logs a user into Backendless. |
| [Logout User](actions/logout-user.md) | GET | Logs out the current Backendless user. |
| [Register User](actions/register-user.md) | POST | Registers a new user in Backendless. |
| [Restore User Password](actions/restore-user-password.md) | GET | Starts password recovery for a Backendless user. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Backendless. |
| [Validate User Login](actions/validate-user-login.md) | GET |  |
| [Validate User Token](actions/validate-user-token.md) | GET | Validates a user token in Backendless. |


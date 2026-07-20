# Backendless: Native API Reference

A consolidated summary of Backendless's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://backendless.com/docs/rest/index.html
- **API base URL:** `{apiUrl}`

## Authentication

### API Key

Connect Backendless with an Application ID, REST API Key, and optional API URL override.

### Credentials

- **API Key:** `apiKey` · required
- **Application ID:** `applicationId` · required · Your Backendless Application ID from Manage > App Settings.
- **API URL:** `apiUrl` · optional · Optional Backendless native API base URL. Leave the default North American endpoint unless your app is hosted in another region.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://backendless.com/docs/rest/setup.html)

## Pagination

Use `pageSize` in the query string to set the page size (default 25). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Append File](actions/append-file.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/files/append/{path}` | [docs](https://backendless.com/docs/rest/file_append.html) |
| [Bulk Create Data Objects](actions/bulk-create-data-objects.md) | `POST /{{credentials.applicationId}}/{{credentials.apiKey}}/data/bulk/{tableName}` | [docs](https://backendless.com/docs/rest/data_multiple_objects_bulk_create.html) |
| [Bulk Delete Data Objects](actions/bulk-delete-data-objects.md) | `DELETE /{{credentials.applicationId}}/{{credentials.apiKey}}/data/bulk/{tableName}` | [docs](https://backendless.com/docs/rest/data_multiple_objects_bulk_delete.html) |
| [Bulk Update Data Objects](actions/bulk-update-data-objects.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/data/bulk/{tableName}` | [docs](https://backendless.com/docs/rest/data_multiple_objects_bulk_update.html) |
| [Check Cache Key](actions/check-cache-key.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/cache/{key}/check` | [docs](https://backendless.com/docs/rest/ut_checking_if_key_exists_in_cach.html) |
| [Compare And Set Counter](actions/compare-and-set-counter.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/counters/{counterName}/get/compareandset` | [docs](https://backendless.com/docs/rest/ut_conditional_update.html) |
| [Copy File Or Folder](actions/copy-file-or-folder.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/files/copy` | [docs](https://backendless.com/docs/rest/file_file_copy.html) |
| [Count Data Objects](actions/count-data-objects.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/data/{tableName}/count` | [docs](https://backendless.com/docs/rest/data_get_object_count.html) |
| [Count Directory Items](actions/count-directory-items.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/files/{path}/` | [docs](https://backendless.com/docs/rest/file_get_file_count.html) |
| [Create Data Object](actions/create-data-object.md) | `POST /{{credentials.applicationId}}/{{credentials.apiKey}}/data/{tableName}` | [docs](https://backendless.com/docs/rest/data_single_object_save.html) |
| [Create Directory](actions/create-directory.md) | `POST /{{credentials.applicationId}}/{{credentials.apiKey}}/files/{directoryPath}/` | [docs](https://backendless.com/docs/rest/file_create_a_file_directory.html) |
| [Decrement Counter](actions/decrement-counter.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/counters/{counterName}/decrement/get` | [docs](https://backendless.com/docs/rest/ut_decrement_by_1__return_current.html) |
| [Delete Cache Value](actions/delete-cache-value.md) | `DELETE /{{credentials.applicationId}}/{{credentials.apiKey}}/cache/{key}` | [docs](https://backendless.com/docs/rest/ut_deleting_object_from_cache.html) |
| [Delete Data Object](actions/delete-data-object.md) | `DELETE /{{credentials.applicationId}}/{{credentials.apiKey}}/data/{tableName}/{objectId}` | [docs](https://backendless.com/docs/rest/data_single_object_deletion.html) |
| [Delete File](actions/delete-file.md) | `DELETE /{{credentials.applicationId}}/{{credentials.apiKey}}/files/{path}/{fileName}` | [docs](https://backendless.com/docs/rest/files_file_deletion.html) |
| [Extend Cache TTL](actions/extend-cache-ttl.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/cache/{key}/expireIn` | [docs](https://backendless.com/docs/rest/ut_extending_objects_life_in_cach.html) |
| [Get Cache Value](actions/get-cache-value.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/cache/{key}` | [docs](https://backendless.com/docs/rest/ut_retrieving_data_from_cache.html) |
| [Get Counter Value](actions/get-counter-value.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/counters/{counterName}` | [docs](https://backendless.com/docs/rest/ut_get_current.html) |
| [Get Data Object](actions/get-data-object.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/data/{tableName}/{objectId}` |  |
| [Get First Data Object](actions/get-first-data-object.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/data/{tableName}/first` | [docs](https://backendless.com/docs/rest/data_basic_search.html) |
| [Get Last Data Object](actions/get-last-data-object.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/data/{tableName}/last` | [docs](https://backendless.com/docs/rest/data_basic_search.html) |
| [Increment Counter](actions/increment-counter.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/counters/{counterName}/increment/get` | [docs](https://backendless.com/docs/rest/ut_increment_by_1__return_current.html) |
| [List Counters](actions/list-counters.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/counters/{counterNamePattern}/list` | [docs](https://backendless.com/docs/rest/ut_get_counters_listing.html) |
| [List Data Objects](actions/list-data-objects.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/data/{tableName}` | [docs](https://backendless.com/docs/rest/data_basic_search.html) |
| [List Directory](actions/list-directory.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/files/{path}/` | [docs](https://backendless.com/docs/rest/file_directory_listing.html) |
| [List Root Directory](actions/list-root-directory.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/files/` | [docs](https://backendless.com/docs/rest/file_directory_listing.html) |
| [Login User](actions/login-user.md) | `POST /{{credentials.applicationId}}/{{credentials.apiKey}}/users/login` | [docs](https://backendless.com/docs/rest/users_login.html) |
| [Logout User](actions/logout-user.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/users/logout` | [docs](https://backendless.com/docs/rest/users_logout.html) |
| [Move File Or Folder](actions/move-file-or-folder.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/files/move` | [docs](https://backendless.com/docs/rest/file_renaming_a_file_director2.html) |
| [Put Cache Value](actions/put-cache-value.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/cache/{key}` | [docs](https://backendless.com/docs/rest/ut_putting_data_into_cache.html) |
| [Register User](actions/register-user.md) | `POST /{{credentials.applicationId}}/{{credentials.apiKey}}/users/register` | [docs](https://backendless.com/docs/rest/users_user_registration.html) |
| [Rename File Or Folder](actions/rename-file-or-folder.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/files/rename` | [docs](https://backendless.com/docs/rest/file_renaming_a_file_directory.html) |
| [Restore User Password](actions/restore-user-password.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/users/restorepassword/{identity}` | [docs](https://backendless.com/docs/rest/users_password_recovery.html) |
| [Save Binary File](actions/save-binary-file.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/files/binary/{filePath}` | [docs](https://backendless.com/docs/rest/file_save_files_from_byte_arrays.html) |
| [Update Data Object](actions/update-data-object.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/data/{tableName}/{objectId}` | [docs](https://backendless.com/docs/rest/data_single_object_update.html) |
| [Update User](actions/update-user.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/users/{userId}` | [docs](https://backendless.com/docs/rest/users_update_user_properties.html) |
| [Upload File](actions/upload-file.md) | `POST /{{credentials.applicationId}}/{{credentials.apiKey}}/files/{path}/{fileName}` | [docs](https://backendless.com/docs/rest/files_file_upload.html) |
| [Upsert Data Object](actions/upsert-data-object.md) | `PUT /{{credentials.applicationId}}/{{credentials.apiKey}}/data/{tableName}/upsert` | [docs](https://backendless.com/docs/rest/data_upsert_single_object.html) |
| [Validate User Login](actions/validate-user-login.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/users/isvalidlogin/{userLogin}` |  |
| [Validate User Token](actions/validate-user-token.md) | `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/users/isvalidusertoken/{userToken}` | [docs](https://backendless.com/docs/rest/users_validating_user_login.html) |

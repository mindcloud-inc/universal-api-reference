# <img src="https://images.mindcloud.co/apps/icons/frappe_1776258325980.png" alt="Frappe logo" width="28" height="28"> Frappe: Universal API

Connect to Frappe sites to manage DocTypes, documents, file uploads, and whitelisted method calls through the official REST and RPC APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/frappe/latest
- **Actions:** 46
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://frappe.io/framework
- **Vendor API docs:** https://docs.frappe.io/framework/user/en/guides/integration/rest_api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Logged User](actions/get-logged-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frappe/latest/actions/get-logged-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (46)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Upload File V1](actions/upload-file-v1.md) | POST | Uploads a file to Frappe. |
| [Upload File V1 Alias](actions/upload-file-v1-alias.md) | POST | Uploads a file to Frappe. |
| [Upload File V2](actions/upload-file-v2.md) | POST | Uploads a file to Frappe. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Login V1](actions/login-v1.md) | POST | Logs in a user to Frappe. |
| [Login V1 Alias](actions/login-v1-alias.md) | POST | Logs in a user to Frappe. |
| [Login V2](actions/login-v2.md) | POST | Logs in a user to Frappe. |
| [Logout V1](actions/logout-v1.md) | DELETE | Logs out the current Frappe user. |
| [Logout V1 Alias](actions/logout-v1-alias.md) | DELETE | Logs out the current Frappe user. |
| [Logout V2](actions/logout-v2.md) | DELETE | Logs out the current Frappe user. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment To Document V2](actions/add-comment-to-document-v2.md) | PUT | Adds a comment to a Frappe document. |
| [Call DocType Controller Method V2 (GET)](actions/call-doctype-controller-method-v2-get.md) | GET | Calls a Frappe DocType controller method with GET. |
| [Call DocType Controller Method V2 (POST)](actions/call-doctype-controller-method-v2-post.md) | POST | Calls a Frappe DocType controller method with POST. |
| [Call Whitelisted Method V1 Alias (GET)](actions/call-whitelisted-method-v1-alias-get.md) | GET | Calls a whitelisted Frappe method with GET. |
| [Call Whitelisted Method V1 Alias (POST)](actions/call-whitelisted-method-v1-alias-post.md) | POST | Calls a whitelisted Frappe method with POST. |
| [Call Whitelisted Method V1 (GET)](actions/call-whitelisted-method-v1-get.md) | GET | Calls a whitelisted Frappe method with GET. |
| [Call Whitelisted Method V1 (POST)](actions/call-whitelisted-method-v1-post.md) | POST | Calls a whitelisted Frappe method with POST. |
| [Call Whitelisted Method V2 (GET)](actions/call-whitelisted-method-v2-get.md) | GET | Calls a whitelisted Frappe method with GET. |
| [Call Whitelisted Method V2 (POST)](actions/call-whitelisted-method-v2-post.md) | POST | Calls a whitelisted Frappe method with POST. |
| [Cancel Document V2](actions/cancel-document-v2.md) | PUT | Cancels a document in a Frappe DocType. |
| [Copy Document V2](actions/copy-document-v2.md) | GET | Retrieves a clean copy of a Frappe document. |
| [Create Document V1](actions/create-document-v1.md) | POST | Creates a new document in a Frappe DocType. |
| [Create Document V1 Alias](actions/create-document-v1-alias.md) | POST | Creates a new document in a Frappe DocType. |
| [Create Document V2](actions/create-document-v2.md) | POST | Creates a new document in a Frappe DocType. |
| [Delete Document V1](actions/delete-document-v1.md) | DELETE | Deletes a document from a Frappe DocType. |
| [Delete Document V1 Alias](actions/delete-document-v1-alias.md) | DELETE | Deletes a document from a Frappe DocType. |
| [Delete Document V2](actions/delete-document-v2.md) | DELETE | Deletes a document from a Frappe DocType. |
| [Get DocType Count V2](actions/get-doctype-count-v2.md) | GET | Retrieves the document count for a Frappe DocType. |
| [Get DocType Metadata V2](actions/get-doctype-metadata-v2.md) | GET | Retrieves metadata for a Frappe DocType. |
| [Get Document V1](actions/get-document-v1.md) | GET | Retrieves a document from a Frappe DocType. |
| [Get Document V1 Alias](actions/get-document-v1-alias.md) | GET | Retrieves a document from a Frappe DocType. |
| [Get Document V2](actions/get-document-v2.md) | GET | Retrieves a document from a Frappe DocType. |
| [List Documents V1](actions/list-documents-v1.md) | GET | Lists documents from a Frappe DocType. |
| [List Documents V1 Alias](actions/list-documents-v1-alias.md) | GET | Lists documents from a Frappe DocType. |
| [List Documents V2](actions/list-documents-v2.md) | GET | Lists documents from a Frappe DocType. |
| [Patch Document V2](actions/patch-document-v2.md) | PUT | Updates a document in Frappe with PATCH. |
| [Ping Site V2](actions/ping-site-v2.md) | GET | Checks the status of a Frappe site. |
| [Put Document V2](actions/put-document-v2.md) | PUT | Updates a document in Frappe with PUT. |
| [Rename Document V2](actions/rename-document-v2.md) | PUT | Renames a document in a Frappe DocType. |
| [Run Doc Method RPC V2](actions/run-doc-method-rpc-v2.md) | PUT | Runs a whitelisted method on a Frappe document. |
| [Run Document Method V2 (GET)](actions/run-document-method-v2-get.md) | GET | Runs a method on a Frappe document with GET. |
| [Run Document Method V2 (POST)](actions/run-document-method-v2-post.md) | PUT | Runs a method on a Frappe document with POST. |
| [Submit Document V2](actions/submit-document-v2.md) | PUT | Submits a document in a Frappe DocType. |
| [Update Document V1](actions/update-document-v1.md) | PUT | Updates a document in a Frappe DocType. |
| [Update Document V1 Alias](actions/update-document-v1-alias.md) | PUT | Updates a document in a Frappe DocType. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Logged User](actions/get-logged-user.md) | GET | Retrieves the logged-in user from Frappe. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Logged User V1 Alias](actions/get-logged-user-v1-alias.md) | GET | Retrieves the logged-in user from Frappe. |


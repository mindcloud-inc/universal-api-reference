# <img src="https://images.mindcloud.co/apps/icons/instant_1776178290751.png" alt="Instant logo" width="28" height="28"> Instant: Universal API

Query, write, and manage Instant data, users, and storage

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/instant/latest
- **Category:** IT Operations / Database
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.instantdb.com
- **Vendor API docs:** https://www.instantdb.com/docs/http-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query Records](actions/query-records.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instant/latest/actions/query-records?connectionId=$CONNECTION_ID&query=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from Instant storage. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Instant storage. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete Files](actions/delete-files.md) | DELETE | Deletes multiple files from Instant storage. |
| [List Files](actions/list-files.md) | GET | Retrieves files from Instant storage. |

### Magic Code

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Magic Code](actions/create-custom-magic-code.md) | POST | Creates a custom magic code in Instant. |
| [Send Magic Code](actions/send-magic-code.md) | POST | Sends a magic code with Instant email. |

### Records

| Action | Method | Description |
| --- | --- | --- |
| [Query Records](actions/query-records.md) | GET | Retrieves records from Instant with an InstaQL query. |
| [Query Records As Email](actions/query-records-as-email.md) | GET | Retrieves records from Instant as a user by email. |
| [Query Records As Guest](actions/query-records-as-guest.md) | GET | Retrieves records from Instant with guest permissions. |
| [Query Records As Refresh Token](actions/query-records-as-refresh-token.md) | GET | Retrieves records from Instant as a user by refresh token. |
| [Query Records With Rule Params](actions/query-records-with-rule-params.md) | GET | Retrieves records from Instant with rule parameters. |

### Room Presence

| Action | Method | Description |
| --- | --- | --- |
| [Get Room Presence](actions/get-room-presence.md) | GET | Retrieves room presence from Instant. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Sign Out Session by Refresh Token](actions/sign-out-session-by-refresh-token.md) | DELETE | Signs out an Instant session by refresh token. |
| [Verify Refresh Token](actions/verify-refresh-token.md) | GET | Verifies an Instant refresh token. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Batch Transact Steps](actions/batch-transact-steps.md) | PUT | Applies transaction steps to Instant records. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Delete User by Email](actions/delete-user-by-email.md) | DELETE | Deletes a user from Instant by email. |
| [Delete User by ID](actions/delete-user-by-id.md) | DELETE | Deletes a user from Instant by ID. |
| [Delete User by Refresh Token](actions/delete-user-by-refresh-token.md) | DELETE | Deletes a user from Instant by refresh token. |
| [Get User by Email](actions/get-user-by-email.md) | GET | Retrieves a user from Instant by email. |
| [Get User by ID](actions/get-user-by-id.md) | GET | Retrieves a user from Instant by ID. |
| [Get User by Refresh Token](actions/get-user-by-refresh-token.md) | GET | Retrieves a user from Instant by refresh token. |

### User Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Refresh Token by Email](actions/create-refresh-token-by-email.md) | POST | Creates a refresh token in Instant by email. |
| [Create Refresh Token by Email With Extra Fields](actions/create-refresh-token-by-email-with-extra-fields.md) | POST | Creates a refresh token in Instant by email, setting extra fields on user creation. |
| [Create Refresh Token by User ID](actions/create-refresh-token-by-user-id.md) | POST | Creates a refresh token in Instant by user ID. |
| [Create Refresh Token by User ID With Extra Fields](actions/create-refresh-token-by-user-id-with-extra-fields.md) | POST | Creates a refresh token in Instant by ID, setting extra fields on creation. |
| [Sign Out User by Email](actions/sign-out-user-by-email.md) | DELETE | Signs out an Instant user by email. |
| [Sign Out User by ID](actions/sign-out-user-by-id.md) | DELETE | Signs out an Instant user by ID. |
| [Verify Magic Code](actions/verify-magic-code.md) | POST | Verifies a magic code in Instant. |
| [Verify Magic Code With Extra Fields](actions/verify-magic-code-with-extra-fields.md) | POST | Verifies a magic code in Instant, setting extra fields on user creation. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Instant. |


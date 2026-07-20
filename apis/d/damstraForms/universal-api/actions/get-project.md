# Damstra Forms: Get Project

Retrieves a project from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-project?connectionId=$CONNECTION_ID&id=1%20or%20ad03b045-7463-49dd-b50c-be59451bcf1f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1 or ad03b045-7463-49dd-b50c-be59451bcf1f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-project?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique id (numeric) or uuid (string) of the project. Example: `1 or ad03b045-7463-49dd-b50c-be59451bcf1f`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `showManaged` | boolean | no | Show/hide the managed attribute. Default: `false`. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "address": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "href": "string",
      "id": 1,
      "inheritWbsItems": true,
      "jobNumber": "string",
      "lockVersion": 1,
      "managed": true,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | From Damstra Forms API example response. |
| `address` | string | From Damstra Forms API example response. |
| `createdAt` | date | From Damstra Forms API example response. |
| `href` | string | From Damstra Forms API example response. |
| `id` | number | From Damstra Forms API example response. |
| `inheritWbsItems` | boolean | From Damstra Forms API example response. |
| `jobNumber` | string | From Damstra Forms API example response. |
| `lockVersion` | number | From Damstra Forms API example response. |
| `managed` | boolean | From Damstra Forms API example response. |
| `name` | string | From Damstra Forms API example response. |
| `updatedAt` | date | From Damstra Forms API example response. |
| `userId` | number | From Damstra Forms API example response. |
| `uuid` | string | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /projects/{id}` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.


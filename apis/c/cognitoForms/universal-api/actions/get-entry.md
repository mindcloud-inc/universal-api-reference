# Cognito Forms: Get Entry



```
GET https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/get-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cognito Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/get-entry?connectionId=$CONNECTION_ID&formId=string&entryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "entryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/get-entry?${params}`, {
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
| `formId` | string | yes | The ID of the Form for which you want to retrieve an Entry |
| `entryId` | string | yes | The ID of the Entry you want to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entry": {
        "action": "string",
        "dateCreated": "2026-05-07T12:00:00.000Z",
        "dateUpdated": "2026-05-07T12:00:00.000Z",
        "role": "string",
        "status": "string"
      },
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entry` | object | Entry metadata and links. |
| `entry.action` | string | Entry action: Submit or Update. |
| `entry.dateCreated` | date | Entry created timestamp. |
| `entry.dateUpdated` | date | Entry updated timestamp. |
| `entry.role` | string | Entry role: Public, Internal, Reviewer. |
| `entry.status` | string | Entry status. |
| `id` | string | The Entry ID. |

## Native endpoint

Through the native Cognito Forms API, this operation is `GET /forms/:formId/entries/:entryId` (base URL `https://www.cognitoforms.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-entry.md) for the provider-specific parameters and requirements.


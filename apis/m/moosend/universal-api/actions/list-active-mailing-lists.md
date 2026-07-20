# Moosend: List Active Mailing Lists

Retrieves active mailing lists from Moosend.

```
GET https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-active-mailing-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-active-mailing-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-active-mailing-lists?${params}`, {
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
| `withStatistics` | string | no | Specifies whether to fetch statistics for the subscribers. Possible values: true (Default) and false . |
| `sortBy` | string | no | The name of the email list property to sort results by. Possible values: Name , Subject , Status , DeliveredOn , and CreatedOn (Default). |
| `sortMethod` | string | no | Specifies the method to sort results. Possible values: DESC for descending and ASC (Default) for ascending. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeMemberCount": 1,
      "bouncedMemberCount": 1,
      "createdBy": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "customFieldsDefinition": [
        {}
      ],
      "id": "string",
      "importOperation": {},
      "name": "Ava Chen",
      "preferences": {},
      "removedMemberCount": 1,
      "status": 1,
      "unsubscribedMemberCount": 1,
      "updatedBy": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeMemberCount` | number |  |
| `bouncedMemberCount` | number |  |
| `createdBy` | string |  |
| `createdOn` | date |  |
| `customFieldsDefinition` | array<object> |  |
| `id` | string |  |
| `importOperation` | object |  |
| `name` | string |  |
| `preferences` | object |  |
| `removedMemberCount` | number |  |
| `status` | number |  |
| `unsubscribedMemberCount` | number |  |
| `updatedBy` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Moosend API, this operation is `GET /lists.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-mailing-lists.md) for the provider-specific parameters and requirements.


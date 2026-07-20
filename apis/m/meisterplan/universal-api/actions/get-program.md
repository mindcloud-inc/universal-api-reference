# Meisterplan: Get Program

Retrieves a program from Meisterplan.

```
GET https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-program
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-program?connectionId=$CONNECTION_ID&scenarioId=string&programId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scenarioId": "string",
  "programId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-program?${params}`, {
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
| `scenarioId` | string | yes | Internal Meisterplan scenario identifier. |
| `programId` | string | yes | Internal Meisterplan program identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finish": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "programKey": "string",
      "rankCategory": {
        "value": "string"
      },
      "start": "2026-05-07T12:00:00.000Z",
      "status": {
        "value": "string"
      },
      "viewUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finish` | date | Program finish date |
| `id` | string | Program ID |
| `name` | string | Program name |
| `programKey` | string | Program key |
| `rankCategory.value` | string | Rank category |
| `start` | date | Program start date |
| `status.value` | string | Program status |
| `viewUrl` | string | View URL |

## Native endpoint

Through the native Meisterplan API, this operation is `GET /scenarios/:scenarioId/programs/:programId` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-program.md) for the provider-specific parameters and requirements.


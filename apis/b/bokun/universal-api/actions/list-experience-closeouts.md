# Bokun: List Experience Closeouts

Retrieves availability closeouts for an experience product from Bokun.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-closeouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-closeouts?connectionId=$CONNECTION_ID&experienceId=1&from=string&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experienceId": "1",
  "from": "string",
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-closeouts?${params}`, {
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
| `experienceId` | number | yes | The Bokun experience ID. |
| `from` | string | yes | The start date in yyyy-MM-dd format. |
| `to` | string | yes | The end date in yyyy-MM-dd format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "startTimeIds": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `startTimeIds` | array<number> |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/availability/:experienceId/closeouts` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-experience-closeouts.md) for the provider-specific parameters and requirements.


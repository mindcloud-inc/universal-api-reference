# Mighty Tix: Delete Session

Deletes an existing session from Mighty Tix.

```
DELETE https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/delete-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Tix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/delete-session?connectionId=$CONNECTION_ID&variables.input=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.input": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/delete-session?${params}`, {
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
| `variables.input` | object | yes | DeleteOneSessionInput object from the Mighty Tix Admin GraphQL docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "2026-05-07T12:00:00.000Z",
      "eventId": "string",
      "id": "string",
      "offsale": "2026-05-07T12:00:00.000Z",
      "onsale": "2026-05-07T12:00:00.000Z",
      "start": "2026-05-07T12:00:00.000Z",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | date |  |
| `eventId` | string |  |
| `id` | string |  |
| `offsale` | date |  |
| `onsale` | date |  |
| `start` | date |  |
| `updated` | date |  |

## Native endpoint

Through the native Mighty Tix API, this operation is `POST admin-api/graphql` (base URL `https://mindcloudmttix260403.mightytix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-session.md) for the provider-specific parameters and requirements.


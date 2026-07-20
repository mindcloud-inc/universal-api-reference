# Airmeet: List Participants

Finds participants in a specific Airmeet event.

```
GET https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/list-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airmeet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/list-participants?connectionId=$CONNECTION_ID&airmeetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "airmeetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/list-participants?${params}`, {
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
| `airmeetId` | string | yes | The Airmeet event ID. |
| `emailIds` | string | no | One or more comma-separated participant email addresses to filter by. |
| `pageNumber` | number | no | Page number of participants to fetch. |
| `resultSize` | number | no | Maximum number of participants to return per page. |
| `sortingDirection` | string | no | Sort direction, typically ASC or DESC. |
| `sortingKey` | string | no | Participant sorting column such as name, email, or registrationDate. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airmeet API returns.

## Native endpoint

Through the native Airmeet API, this operation is `GET /airmeet/{airmeetId}/participants` (base URL `https://api-gateway-prod.us.airmeet.com/prod`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-participants.md) for the provider-specific parameters and requirements.


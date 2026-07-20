# Vouchsafe: Perform Adverse Media Check

Runs an adverse media check in Vouchsafe.

```
POST https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/perform-adverse-media-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchsafe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/perform-adverse-media-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/perform-adverse-media-check', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | Given name. |
| `middleNames` | string | no | Middle name(s), space-separated. |
| `lastName` | string | yes | Family name. |
| `location` | string | no | City, county, or country. Strongly recommended to improve precision. |
| `threshold` | number | no | Adversity score threshold from 0 to 100. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchsafe API returns.

## Native endpoint

Through the native Vouchsafe API, this operation is `POST /adverse-media` (base URL `https://app.vouchsafe.id/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/perform-adverse-media-check.md) for the provider-specific parameters and requirements.


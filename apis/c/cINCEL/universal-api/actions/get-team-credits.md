# CINCEL: Get Team Credits



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-team-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-team-credits?connectionId=$CONNECTION_ID&team=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "team": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-team-credits?${params}`, {
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
| `team` | string | yes | UUID of the team whose credits should be retrieved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docs": {},
      "gbgVerfications": {},
      "kyc": {},
      "timestamps": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docs` | object | Document credit totals grouped by source and usage. |
| `gbgVerfications` | object | GBG verification credit totals when present. |
| `kyc` | object | KYC credit totals grouped by source and usage. |
| `timestamps` | object | Timestamp credit totals grouped by source and usage. |

## Native endpoint

Through the native CINCEL API, this operation is `GET /teams/:team/credits` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-credits.md) for the provider-specific parameters and requirements.


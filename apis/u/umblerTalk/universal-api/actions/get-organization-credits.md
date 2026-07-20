# Umbler Talk: Get Organization Credits

Retrieves organization conversation limits from Umbler Talk.

```
GET https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-organization-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-organization-credits?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-organization-credits?${params}`, {
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
| `id` | string | yes | The organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organization": {},
      "packages": [
        {}
      ],
      "remainingCredits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organization` | object |  |
| `packages` | array<object> |  |
| `remainingCredits` | number |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `GET /v1/organizations/[:id]/credits/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-credits.md) for the provider-specific parameters and requirements.


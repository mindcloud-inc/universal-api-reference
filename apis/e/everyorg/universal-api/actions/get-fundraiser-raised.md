# Every.org: Get Fundraiser Raised

Retrieves raised totals for a fundraiser from Every.org.

```
GET https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/get-fundraiser-raised
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Every.org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/get-fundraiser-raised?connectionId=$CONNECTION_ID&nonprofitIdentifier=string&fundraiserIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nonprofitIdentifier": "string",
  "fundraiserIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/get-fundraiser-raised?${params}`, {
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
| `nonprofitIdentifier` | string | yes | A nonprofit slug, EIN, nonprofit ID, or special-fundraiser for multi-nonprofit fundraisers. |
| `fundraiserIdentifier` | string | yes | Fundraiser slug or identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "goalAmount": "string",
      "goalType": "string",
      "raised": "string",
      "supporters": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `goalAmount` | string |  |
| `goalType` | string |  |
| `raised` | string |  |
| `supporters` | number |  |

## Native endpoint

Through the native Every.org API, this operation is `GET /nonprofit/:nonprofitIdentifier/fundraiser/:fundraiserIdentifier/raised` (base URL `https://partners.every.org/v0.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fundraiser-raised.md) for the provider-specific parameters and requirements.


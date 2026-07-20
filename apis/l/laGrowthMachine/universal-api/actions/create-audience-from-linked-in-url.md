# LaGrowthMachine: Create Audience from LinkedIn URL

Creates an audience in LaGrowthMachine from a LinkedIn URL.

```
POST https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/create-audience-from-linked-in-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaGrowthMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/create-audience-from-linked-in-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audience": "string",
  "identityId": "string",
  "linkedinUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/create-audience-from-linked-in-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audience": "string",
    "identityId": "string",
    "linkedinUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audience` | string | yes | Audience name to populate from the LinkedIn search or post. |
| `identityId` | string | yes | Identity ID used to impersonate the LinkedIn search query. |
| `linkedinPostCategory` | string | no | Post interaction category when importing from a LinkedIn post. |
| `linkedinUrl` | string | yes | LinkedIn regular search URL, Sales Navigator search URL, or LinkedIn post URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `statusCode` | number | Provider status code returned after the audience import request. |

## Native endpoint

Through the native LaGrowthMachine API, this operation is `POST /audiences` (base URL `https://apiv2.lagrowthmachine.com/flow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-audience-from-linked-in-url.md) for the provider-specific parameters and requirements.


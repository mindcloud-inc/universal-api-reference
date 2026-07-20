# Fibery: Get Temporary Public File URLs

Retrieves temporary public file URLs from Fibery.

```
GET https://connect.mindcloud.co/v1/universal/fibery/latest/actions/get-temporary-public-file-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fibery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/get-temporary-public-file-urls?connectionId=$CONNECTION_ID&secrets%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "secrets[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fibery/latest/actions/get-temporary-public-file-urls?${params}`, {
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
| `secrets[]` | array<string> | yes | Array of file secrets to sign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |

## Native endpoint

Through the native Fibery API, this operation is `POST /files/sign-urls` (base URL `https://{{credentials.account}}.fibery.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-temporary-public-file-urls.md) for the provider-specific parameters and requirements.


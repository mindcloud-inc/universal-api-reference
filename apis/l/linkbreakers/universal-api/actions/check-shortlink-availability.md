# Linkbreakers: Check Shortlink Availability

Checks whether a shortlink is available in Linkbreakers.

```
GET https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/check-shortlink-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/check-shortlink-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/check-shortlink-availability?${params}`, {
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
| `shortlink` | string | no | The shortlink slug to check. |
| `customDomainId` | string | no | The custom domain ID to check against. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | boolean | Whether the requested shortlink slug is available for use. |

## Native endpoint

Through the native Linkbreakers API, this operation is `GET /v1/links/shortlink-availability` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-shortlink-availability.md) for the provider-specific parameters and requirements.


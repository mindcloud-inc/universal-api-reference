# Windsor.ai: Generate Authorization Link For Any Data Source

Generates a Windsor.ai authorization link for any data source.

```
GET https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/generate-authorization-link-for-any-data-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Windsor.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/generate-authorization-link-for-any-data-source?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/generate-authorization-link-for-any-data-source?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | Generated Windsor.ai co-user authorization URL. |

## Native endpoint

Through the native Windsor.ai API, this operation is `GET /api/team/generate-co-user-url` (base URL `https://onboard.windsor.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-authorization-link-for-any-data-source.md) for the provider-specific parameters and requirements.


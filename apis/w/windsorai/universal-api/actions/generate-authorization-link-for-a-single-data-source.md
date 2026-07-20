# Windsor.ai: Generate Authorization Link For A Single Data Source

Generates a Windsor.ai authorization link for one data source.

```
GET https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/generate-authorization-link-for-a-single-data-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Windsor.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/generate-authorization-link-for-a-single-data-source?connectionId=$CONNECTION_ID&allowedSources=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "allowedSources": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/generate-authorization-link-for-a-single-data-source?${params}`, {
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
| `allowedSources` | string | yes | Restrict the generated authorization link to one Windsor.ai source ID. |

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
| `url` | string | Generated Windsor.ai co-user authorization URL restricted to the requested source. |

## Native endpoint

Through the native Windsor.ai API, this operation is `GET /api/team/generate-co-user-url/` (base URL `https://onboard.windsor.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-authorization-link-for-a-single-data-source.md) for the provider-specific parameters and requirements.


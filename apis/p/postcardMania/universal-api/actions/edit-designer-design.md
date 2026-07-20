# PostcardMania: Edit Designer Design

Retrieves an edit session for a PostcardMania design.

```
GET https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/edit-designer-design
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/edit-designer-design?connectionId=$CONNECTION_ID&designID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "designID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/edit-designer-design?${params}`, {
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
| `designID` | number | yes | Internal design identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "designID": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `designID` | number | Resolved design identifier for the editor session. |
| `url` | string | Designer editor URL for the requested design. |

## Native endpoint

Through the native PostcardMania API, this operation is `GET /design/{{designID}}/edit` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-designer-design.md) for the provider-specific parameters and requirements.


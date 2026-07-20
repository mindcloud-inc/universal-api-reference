# PostcardMania: List Design Tags

Retrieves tags for a PostcardMania design.

```
GET https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/list-design-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/list-design-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/list-design-tags?${params}`, {
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
| `designID` | string | no | Internal design identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tagGroup": "string",
      "tagID": 1,
      "tagName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tagGroup` | string | Tag group. |
| `tagID` | number | Tag identifier. |
| `tagName` | string | Tag name. |

## Native endpoint

Through the native PostcardMania API, this operation is `GET /gallery/tags/{{designID}}` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-design-tags.md) for the provider-specific parameters and requirements.


# RollWorks: List Valid and Invalid Segments for Crosschannel LAL Targeting

Retrieves valid and invalid segments for RollWorks crosschannel LAL targeting.

```
GET https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/list-valid-and-invalid-segments-for-crosschannel-lal-targeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RollWorks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/list-valid-and-invalid-segments-for-crosschannel-lal-targeting?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/list-valid-and-invalid-segments-for-crosschannel-lal-targeting?${params}`, {
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
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native RollWorks API, this operation is `GET /audience/v1/crosschannel_lal_segments/valid-segments` (base URL `https://services.adroll.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-valid-and-invalid-segments-for-crosschannel-lal-targeting.md) for the provider-specific parameters and requirements.


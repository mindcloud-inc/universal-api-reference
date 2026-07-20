# Nationalize_io Universal API Examples

These examples use the MindCloud API key and Nationalize_io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Predict Nationality by Name

Retrieves nationality predictions from Nationalize.io for one name.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalizeIo/latest/actions/predict-nationality-by-name?connectionId=$CONNECTION_ID&name=johnson" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "johnson"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalizeIo/latest/actions/predict-nationality-by-name?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "country": [
        {
          "countryId": "string",
          "probability": 1
        }
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Predict Nationality by Name action reference](actions/predict-nationality-by-name.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nationalizeIo/latest/actions/predict-nationality-by-name).

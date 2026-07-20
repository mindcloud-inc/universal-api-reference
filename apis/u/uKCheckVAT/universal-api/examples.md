# UK Check VAT Universal API Examples

These examples use the MindCloud API key and UK Check VAT connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check VAT Registration



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uKCheckVAT/latest/actions/check-vat-registration?connectionId=$CONNECTION_ID&targetVrn=553557881" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "targetVrn": "553557881"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uKCheckVAT/latest/actions/check-vat-registration?${params}`, {
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
      "processingDate": "2026-05-07T12:00:00.000Z",
      "target": {
        "address": {
          "countryCode": "string",
          "line1": "string",
          "postcode": "string"
        },
        "name": "Ava Chen",
        "vatNumber": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Check VAT Registration action reference](actions/check-vat-registration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uKCheckVAT/latest/actions/check-vat-registration).

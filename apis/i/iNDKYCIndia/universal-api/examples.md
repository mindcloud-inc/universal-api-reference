# IN-D KYC India Universal API Examples

These examples use the MindCloud API key and IN-D KYC India connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Classify ID Document

Retrieves ID document classification results from IN-D KYC India.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/classify-id-document?connectionId=$CONNECTION_ID&filename=sample.png&payload=iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mP8%2Fx8AAwMCAO%2B%2Fp9sAAAAASUVORK5CYII%3D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filename": "sample.png",
  "payload": "iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mP8/x8AAwMCAO+/p9sAAAAASUVORK5CYII="
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/classify-id-document?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Classify ID Document action reference](actions/classify-id-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iNDKYCIndia/latest/actions/classify-id-document).

## Generate UID

Creates a new KYC session UID in IN-D KYC India.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/generate-uid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/generate-uid', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "desc": "string",
      "result": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate UID action reference](actions/generate-uid.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iNDKYCIndia/latest/actions/generate-uid).

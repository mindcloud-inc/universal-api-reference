# Edusign Universal API Examples

These examples use the MindCloud API key and Edusign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get School

Retrieves your school details from Edusign.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-school?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-school?${params}`, {
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
      "result": {
        "absencesType": [
          {
            "id": 1,
            "name": "Ava Chen"
          }
        ],
        "city": "string",
        "connector": "string",
        "country": "string",
        "id": "string",
        "language": "string",
        "logo": "string",
        "logos": [
          {
            "filename": "Ava Chen",
            "url": "https://example.com"
          }
        ],
        "name": "Ava Chen",
        "nbCreditsDocumentLeft": 1,
        "phone": "string",
        "postalcode": "string",
        "signatureNb": 1,
        "streetAddress": "string",
        "timezone": "string",
        "webhooks": [
          {
            "type": "string",
            "url": "https://example.com"
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get School action reference](actions/get-school.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/edusign/latest/actions/get-school).

## Add Students Or Professors To Training

Adds students or professors to a training in Edusign.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/add-students-or-professors-to-training" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trainingId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edusign/latest/actions/add-students-or-professors-to-training', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trainingId": "string"
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
      "result": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Students Or Professors To Training action reference](actions/add-students-or-professors-to-training.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/edusign/latest/actions/add-students-or-professors-to-training).

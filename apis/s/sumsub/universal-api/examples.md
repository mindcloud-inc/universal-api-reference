# Sumsub Universal API Examples

These examples use the MindCloud API key and Sumsub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Verification Levels



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/list-verification-levels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/list-verification-levels?${params}`, {
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
      "applicantType": "string",
      "autoCheckGeneratorSettings": {
        "autoCheckMode": "string"
      },
      "clientId": "string",
      "created": {
        "clientSubject": "string",
        "date": "string"
      },
      "createdAt": "string",
      "createdBy": "string",
      "crossCheckPresetId": "string",
      "desc": "string",
      "id": "string",
      "modified": {
        "clientSubject": "string",
        "date": "string"
      },
      "modifiedAt": "string",
      "name": "Ava Chen",
      "requiredIdDocs": {
        "docSets": [
          {
            "idDocSetType": "string",
            "videoRequired": "string"
          }
        ]
      },
      "type": "string",
      "websdkNext": true
    }
  ],
  "meta": {}
}
```

See the full [List Verification Levels action reference](actions/list-verification-levels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sumsub/latest/actions/list-verification-levels).

## Add Applicant Note



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/add-applicant-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "applicantId": "69e9345fee2635bd19c36a69",
  "note": "Disposable sandbox note from MindCloud Codex."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/add-applicant-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "applicantId": "69e9345fee2635bd19c36a69",
    "note": "Disposable sandbox note from MindCloud Codex."
  })
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

See the full [Add Applicant Note action reference](actions/add-applicant-note.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sumsub/latest/actions/add-applicant-note).

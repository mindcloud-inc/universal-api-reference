# Jaicob Universal API Examples

These examples use the MindCloud API key and Jaicob connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Candidates



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/list-candidates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/list-candidates?${params}`, {
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
      "applicantDetails": {},
      "certifications": [
        {}
      ],
      "description": "string",
      "educations": [
        {}
      ],
      "function": "string",
      "id": "string",
      "languages": [
        {}
      ],
      "skills": [
        {}
      ],
      "status": "string",
      "tags": [
        "string"
      ],
      "workExperiences": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Candidates action reference](actions/list-candidates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jaicob/latest/actions/list-candidates).

## Create Application



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vacancyId": "string",
  "applicantDetails": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-application', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vacancyId": "string",
    "applicantDetails": {}
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Application action reference](actions/create-application.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jaicob/latest/actions/create-application).

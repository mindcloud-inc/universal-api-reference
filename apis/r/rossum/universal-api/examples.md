# Rossum Universal API Examples

These examples use the MindCloud API key and Rossum connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Current User

Retrieves the current user from Rossum.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-current-user?${params}`, {
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
      "authType": "string",
      "dateJoined": "string",
      "deleted": true,
      "email": "ava@example.com",
      "emailVerified": true,
      "firstName": "Ava",
      "groups": [
        "string"
      ],
      "id": 1,
      "isActive": true,
      "lastLogin": "string",
      "lastName": "Chen",
      "oidcId": {},
      "organization": "string",
      "phoneNumber": "string",
      "uiSettings": {
        "complexLineItems": true,
        "dashboard": {
          "workspacesSorting": "string"
        },
        "isUsingNewDashboard": true,
        "locale": "string",
        "onboardingAcknowledged": true,
        "onboardingSurvey": {
          "activeStep": "string",
          "stepsData": {
            "whatIsYourRole": {
              "selectedOptions": [
                "string"
              ]
            }
          }
        },
        "showConfidenceScore": true
      },
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Current User action reference](actions/retrieve-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rossum/latest/actions/retrieve-current-user).

## Assign Annotation

Assigns assignees to an annotation in Rossum.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/assign-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "annotations[]": [
    "string"
  ],
  "assignees[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rossum/latest/actions/assign-annotation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "annotations[]": ["string"],
    "assignees[]": ["string"]
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

See the full [Assign Annotation action reference](actions/assign-annotation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rossum/latest/actions/assign-annotation).

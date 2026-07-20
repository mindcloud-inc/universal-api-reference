# SonarQube Universal API Examples

These examples use the MindCloud API key and SonarQube connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Authentication

Retrieves SonarQube authentication validation results.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/validate-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/validate-authentication?${params}`, {
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
      "valid": true
    }
  ],
  "meta": {}
}
```

See the full [Validate Authentication action reference](actions/validate-authentication.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sonarQube/latest/actions/validate-authentication).

## Activate Quality Profile Rule

Updates a quality profile rule in SonarQube.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/activate-quality-profile-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/activate-quality-profile-rule', {
  method: 'PUT',
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
      "response": {},
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Activate Quality Profile Rule action reference](actions/activate-quality-profile-rule.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sonarQube/latest/actions/activate-quality-profile-rule).

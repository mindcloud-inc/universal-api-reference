# LaunchDarkly Universal API Examples

These examples use the MindCloud API key and LaunchDarkly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from LaunchDarkly.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-projects?${params}`, {
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
      "defaultClientSideAvailability": {},
      "id": "string",
      "includeInSnippetByDefault": true,
      "key": "string",
      "links": {},
      "name": "Ava Chen",
      "requireViewAssociationForNewFlags": true,
      "requireViewAssociationForNewSegments": true,
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/launchDarkly/latest/actions/list-projects).

## Copy Feature Flag

Copies feature flag settings between LaunchDarkly environments.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/copy-feature-flag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "featureFlagKey": "string",
  "projectKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/copy-feature-flag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "featureFlagKey": "string",
    "projectKey": "string"
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
      "archived": true,
      "clientSideAvailability": {},
      "creationDate": 1,
      "customProperties": {},
      "defaults": {},
      "deprecated": true,
      "description": "string",
      "environments": {},
      "experiments": {},
      "goalIds": [
        "string"
      ],
      "includeInSnippet": true,
      "key": "string",
      "kind": "string",
      "links": {},
      "name": "Ava Chen",
      "tags": [
        "string"
      ],
      "temporary": true,
      "variations": [
        {}
      ],
      "version": 1
    }
  ],
  "meta": {}
}
```

See the full [Copy Feature Flag action reference](actions/copy-feature-flag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/launchDarkly/latest/actions/copy-feature-flag).

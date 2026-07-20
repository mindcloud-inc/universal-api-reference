# SportsData Universal API Examples

These examples use the MindCloud API key and SportsData connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## NFL Team Profiles

Retrieves active NFL team profiles from SportsData.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/n-fl-team-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/n-fl-team-profiles?${params}`, {
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
      "averageDraftPosition": 1,
      "averageDraftPosition2QB": 1,
      "averageDraftPositionDynasty": 1,
      "averageDraftPositionPPR": 1,
      "byeWeek": 1,
      "city": "string",
      "conference": "string",
      "defensiveCoordinator": "string",
      "defensiveScheme": "string",
      "division": "string",
      "draftKingsName": "Ava Chen",
      "draftKingsPlayerID": 1,
      "fanDuelName": "Ava Chen",
      "fanDuelPlayerID": 1,
      "fantasyDraftName": "Ava Chen",
      "fantasyDraftPlayerID": 1,
      "fullName": "Ava Chen",
      "globalTeamID": 1,
      "headCoach": "string",
      "key": "string",
      "name": "Ava Chen",
      "offensiveCoordinator": "string",
      "offensiveScheme": "string",
      "playerID": 1,
      "primaryColor": "string",
      "quaternaryColor": "string",
      "secondaryColor": "string",
      "specialTeamsCoach": "string",
      "stadiumDetails": {
        "capacity": 1,
        "city": "string",
        "country": "string",
        "geoLat": 1,
        "geoLong": 1,
        "name": "Ava Chen",
        "playingSurface": "string",
        "stadiumID": 1,
        "state": "string",
        "type": "string"
      },
      "stadiumID": 1,
      "teamID": 1,
      "tertiaryColor": "string",
      "upcomingDraftKingsSalary": 1,
      "upcomingFanDuelSalary": 1,
      "upcomingOpponent": "string",
      "upcomingOpponentPositionRank": 1,
      "upcomingOpponentRank": 1,
      "upcomingSalary": 1,
      "upcomingYahooSalary": 1,
      "wikipediaLogoUrl": "https://example.com",
      "wikipediaWordMarkUrl": "https://example.com",
      "yahooName": "Ava Chen",
      "yahooPlayerID": 1
    }
  ],
  "meta": {}
}
```

See the full [NFL Team Profiles action reference](actions/n-fl-team-profiles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sportsData/latest/actions/n-fl-team-profiles).

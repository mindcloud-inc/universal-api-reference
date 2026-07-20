# Create Session with CoachAccountable

Creates a session in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Create Session](https://www.coachaccountable.com/APIDocs#Session.add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | — |
| `title` | body | `string` | yes | Maximum length: 200. |
| `dateOf` | body | `date` | yes | — |
| `timeOf` | body | `string` | yes | — |
| `content` | body | `string` | yes | Maximum length: 100000. |
| `keyInsightSet` | body | `string` | no | A newline-separated list of Key Insights to be part of the Session Notes, one per line. By prepending an item with an asterisk (*), the Key Insight will be starred. |
| `visibility` | body | `list` | no | Accepted values: `*`, `C`, `P`. |

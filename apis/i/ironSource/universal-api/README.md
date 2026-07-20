# <img src="https://images.mindcloud.co/apps/icons/ironsource-icon_1777304314946.png" alt="ironSource logo" width="28" height="28"> ironSource: Universal API

Build automations and reporting workflows for Unity LevelPlay / ironSource Ads, including applications, monetization reports, ad units, mediation groups, network instances, placements, impression-level revenue reports, and Ad Quality raw-data report URLs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ironSource/latest
- **Category:** Marketing
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.is.com/
- **Vendor API docs:** https://docs.unity.com/en-us/grow/levelplay/platform/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Bearer Token](actions/get-bearer-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-bearer-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Bearer Token](actions/get-bearer-token.md) | GET | Retrieves a bearer token from ironSource. |

### Ad Unit

| Action | Method | Description |
| --- | --- | --- |
| [Create Ad Units](actions/create-ad-units.md) | POST | Creates new ad units in ironSource. |
| [Get Ad Units](actions/get-ad-units.md) | GET | Retrieves ad units from ironSource. |
| [Update Ad Units](actions/update-ad-units.md) | PUT | Updates existing ad units in ironSource. |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Create Application](actions/create-application.md) | POST | Creates a new application in ironSource. |
| [List Applications](actions/list-applications.md) | GET | Lists applications in ironSource. |

### Impression Level Revenue Report Url

| Action | Method | Description |
| --- | --- | --- |
| [Get Impression Level Revenue Report URL](actions/get-impression-level-revenue-report-url.md) | GET | Retrieves an impression-level revenue report URL from ironSource. |

### Mediation Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Mediation Groups](actions/create-mediation-groups.md) | POST | Creates new mediation groups in ironSource. |
| [Delete Mediation Groups](actions/delete-mediation-groups.md) | DELETE | Deletes existing mediation groups from ironSource. |
| [Get Mediation Groups](actions/get-mediation-groups.md) | GET | Retrieves mediation groups from ironSource. |
| [Update Mediation Groups](actions/update-mediation-groups.md) | PUT | Updates existing mediation groups in ironSource. |

### Network Instance

| Action | Method | Description |
| --- | --- | --- |
| [Create Network Instances](actions/create-network-instances.md) | POST | Creates new network instances in ironSource. |
| [Delete Network Instances](actions/delete-network-instances.md) | DELETE | Deletes existing network instances from ironSource. |
| [Get Network Instances](actions/get-network-instances.md) | GET | Retrieves network instances from ironSource. |
| [Update Network Instances](actions/update-network-instances.md) | PUT | Updates existing network instances in ironSource. |

### Placement

| Action | Method | Description |
| --- | --- | --- |
| [Create Placements](actions/create-placements.md) | POST | Creates new placements in ironSource. |
| [Delete Placement](actions/delete-placement.md) | DELETE | Deletes an existing placement from ironSource by archiving it. |
| [Get Placements](actions/get-placements.md) | GET | Retrieves placements from ironSource. |
| [Update Placements](actions/update-placements.md) | PUT | Updates existing placements in ironSource. |

### Reporting Row

| Action | Method | Description |
| --- | --- | --- |
| [Get Reporting](actions/get-reporting.md) | GET | Retrieves reporting data from ironSource. |

### User Ad Revenue Report Url

| Action | Method | Description |
| --- | --- | --- |
| [Get User Ad Revenue Report URL](actions/get-user-ad-revenue-report-url.md) | GET | Retrieves a user ad revenue report URL from ironSource. |


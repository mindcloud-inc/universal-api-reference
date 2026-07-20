# <img src="https://images.mindcloud.co/apps/icons/zoho-assist_1774038191221.png" alt="Zoho Assist logo" width="28" height="28"> Zoho Assist: Universal API

Zoho Assist is Zoho's remote support and unattended access platform for starting support sessions, managing unattended devices and groups, and retrieving session reports.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoAssist/latest
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://assist.zoho.com/
- **Vendor API docs:** https://www.zoho.com/assist/api/introduction.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Device

| Action | Method | Description |
| --- | --- | --- |
| [List Unattended Computers](actions/list-unattended-computers.md) | GET | Lists unattended computers configured in Zoho Assist. |
| [Update Unattended Computer](actions/update-unattended-computer.md) | PUT | Updates the display name of an unattended computer in Zoho Assist. |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Delete Unattended Computer](actions/delete-unattended-computer.md) | DELETE | Deletes an unattended computer from Zoho Assist. |
| [Get Device Details](actions/get-device-details.md) | GET | Gets details for an unattended device in Zoho Assist. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Unattended Group](actions/create-unattended-group.md) | POST | Creates a new unattended computer group in Zoho Assist. |
| [List Unattended Groups](actions/list-unattended-groups.md) | GET | Lists existing unattended computer groups in Zoho Assist. |
| [Update Unattended Group](actions/update-unattended-group.md) | PUT | Updates an existing unattended computer group in Zoho Assist. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Delete Unattended Group](actions/delete-unattended-group.md) | DELETE | Deletes existing unattended computer groups from Zoho Assist. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List Session Reports](actions/list-session-reports.md) | GET | Lists reports for previously conducted Zoho Assist sessions. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST | Creates a remote support or screen sharing session in Zoho Assist. |
| [Create Unattended Session](actions/create-unattended-session.md) | POST | Creates an unattended remote session for a Zoho Assist device. |
| [Schedule Session](actions/schedule-session.md) | POST | Schedules a remote support or screen sharing session in Zoho Assist. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Gets details for the current Zoho Assist user. |


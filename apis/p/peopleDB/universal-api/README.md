# <img src="https://images.mindcloud.co/apps/icons/people-db_1775734930880.png" alt="PeopleDB logo" width="28" height="28"> PeopleDB: Universal API

PeopleDB is a contact intelligence API for retrieving professional contact information by LinkedIn or GitHub identity and for validating email addresses.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/peopleDB/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://peopledb.co
- **Vendor API docs:** https://docs.peopledb.co

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contact Info by GitHub Username](actions/get-contact-info-by-git-hub-username.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDB/latest/actions/get-contact-info-by-git-hub-username?connectionId=$CONNECTION_ID&githubLogin=e.g.%20dhh" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Info by GitHub ID](actions/get-contact-info-by-git-hub-id.md) | GET | Retrieves contact info from PeopleDB by GitHub ID. |
| [Get Contact Info by GitHub Username](actions/get-contact-info-by-git-hub-username.md) | GET | Retrieves contact info from PeopleDB by GitHub username. |
| [Get Contact Info by LinkedIn ID](actions/get-contact-info-by-linked-in-id.md) | GET | Retrieves contact info from PeopleDB by LinkedIn ID. |
| [Get Contact Info by LinkedIn Username](actions/get-contact-info-by-linked-in-username.md) | GET | Retrieves contact info from PeopleDB by LinkedIn username. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email Address](actions/validate-email-address.md) | GET | Validates an email address in PeopleDB. |
| [Validate Email Address via POST](actions/validate-email-address-post.md) | POST | Validates an email address in PeopleDB via POST. |


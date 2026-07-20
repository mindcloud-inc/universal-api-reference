# <img src="https://images.mindcloud.co/apps/icons/teachrlogo200x25-en-1_1775162382963.png" alt="Teachlr Organizations logo" width="28" height="28"> Teachlr Organizations: Universal API

Create courses, manage learners, and issue certificates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/teachlrOrganizations/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://organizaciones.teachlr.com/
- **Vendor API docs:** https://soporte.teachlr.com/article-categories/documentacion-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User by Email](actions/get-user-by-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/get-user-by-email?connectionId=$CONNECTION_ID&email=apps%40mindcloud.co" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Career

| Action | Method | Description |
| --- | --- | --- |
| [Get Career Details Full](actions/get-career-details-full.md) | GET |  |
| [List Careers](actions/list-careers.md) | GET |  |
| [List Careers With Active Coupons](actions/list-careers-with-active-coupons.md) | GET |  |
| [List Paginated Careers Without Embedded Courses](actions/list-paginated-careers-without-embedded-courses.md) | GET |  |
| [List Public Library Careers](actions/list-public-library-careers.md) | GET |  |

### Course

| Action | Method | Description |
| --- | --- | --- |
| [Get Course Details Full](actions/get-course-details-full.md) | GET |  |
| [Get Course Details Localized](actions/get-course-details-localized.md) | GET |  |
| [List Active Courses](actions/list-active-courses.md) | GET |  |
| [List All Non-Expired Courses](actions/list-all-non-expired-courses.md) | GET |  |
| [List Courses By Career](actions/list-courses-by-career.md) | GET |  |
| [List Courses By Category And Subcategory](actions/list-courses-by-category-and-subcategory.md) | GET |  |
| [List Courses By Instructor](actions/list-courses-by-instructor.md) | GET |  |
| [List Courses With Active Coupons](actions/list-courses-with-active-coupons.md) | GET |  |
| [List Deactivated Courses](actions/list-deactivated-courses.md) | GET |  |
| [List Draft Courses](actions/list-draft-courses.md) | GET |  |
| [List Paginated Courses](actions/list-paginated-courses.md) | GET |  |
| [List Pending Courses](actions/list-pending-courses.md) | GET |  |
| [List Public Library Courses](actions/list-public-library-courses.md) | GET |  |
| [Search And Sort Courses](actions/search-and-sort-courses.md) | GET |  |

### Meeting

| Action | Method | Description |
| --- | --- | --- |
| [Create Meeting](actions/create-meeting.md) | POST |  |
| [Delete Meeting](actions/delete-meeting.md) | DELETE |  |
| [Update Meeting](actions/update-meeting.md) | PUT |  |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Filter And Export Transactions](actions/filter-and-export-transactions.md) | GET |  |
| [List Transactions](actions/list-transactions.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User by Email](actions/get-user-by-email.md) | GET |  |
| [Get User By Employee Number](actions/get-user-by-employee-number.md) | GET |  |
| [Get User By External Id](actions/get-user-by-external-id.md) | GET |  |
| [Get User By Identifier With Certificates](actions/get-user-by-identifier-with-certificates.md) | GET |  |
| [Get User By Username](actions/get-user-by-username.md) | GET |  |
| [Get User By Username With Certificates](actions/get-user-by-username-with-certificates.md) | GET |  |
| [Get User By Username Without Teaching](actions/get-user-by-username-without-teaching.md) | GET |  |
| [Invite Administrator](actions/invite-administrator.md) | POST |  |
| [Invite Instructor](actions/invite-instructor.md) | POST |  |
| [Invite User And Add To Groups](actions/invite-user-and-add-to-groups.md) | POST |  |
| [Invite User And Subscribe To Careers](actions/invite-user-and-subscribe-to-careers.md) | POST |  |
| [Invite User And Subscribe To Courses](actions/invite-user-and-subscribe-to-courses.md) | POST |  |
| [Invite User And Sync Profile Fields](actions/invite-user-and-sync-profile-fields.md) | POST |  |
| [Invite User With Role](actions/invite-user-with-role.md) | POST |  |


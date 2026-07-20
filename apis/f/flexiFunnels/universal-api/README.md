# <img src="https://images.mindcloud.co/apps/icons/c3f5cba2-56d7-42c0-82bb-d2abfed36dfa-2_1776820547364.png" alt="FlexiFunnels logo" width="28" height="28"> FlexiFunnels: Universal API

FlexiFunnels Membership API for authenticated end-users. The published docs expose member-focused auth, profile, course, lesson, and product endpoints rather than seller/admin management endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/flexiFunnels/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://flexifunnels.com
- **Vendor API docs:** https://bridge.flexifunnels.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexiFunnels/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | GET | Authenticates a FlexiFunnels member. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Course Complete Percentage](actions/course-complete-percentage.md) | GET | Retrieves course completion percentages from FlexiFunnels. |
| [Get Courses](actions/get-courses.md) | GET | Retrieves courses from FlexiFunnels. |
| [Get Custom Script](actions/get-custom-script.md) | GET | Retrieves custom script content from FlexiFunnels. |
| [Get Footer](actions/get-footer.md) | GET | Retrieves footer content from FlexiFunnels. |
| [Get Gamify Points](actions/get-gamify-points.md) | GET | Retrieves gamification points from FlexiFunnels. |
| [Get Goals](actions/get-goals.md) | GET | Retrieves goals from FlexiFunnels. |
| [Get Lesson Details](actions/get-lesson-details.md) | GET | Retrieves lesson details from FlexiFunnels. |
| [Get Lesson Notes](actions/get-lesson-notes.md) | GET | Retrieves lesson notes from FlexiFunnels. |
| [Get Lessons](actions/get-lessons.md) | GET | Retrieves lessons from FlexiFunnels. |
| [Get Member Points](actions/get-member-points.md) | GET | Retrieves member points from FlexiFunnels. |
| [Get Next Badge](actions/get-next-badge.md) | GET | Retrieves the next badge from FlexiFunnels. |
| [Get Quiz List](actions/get-quiz-list.md) | GET | Retrieves quizzes from FlexiFunnels. |
| [Mark Complete](actions/mark-complete.md) | PUT | Marks a lesson complete in FlexiFunnels. |
| [Member Badge List](actions/member-badge-list.md) | GET | Retrieves member badges from FlexiFunnels. |
| [Member Reward List](actions/member-reward-list.md) | GET | Retrieves member rewards from FlexiFunnels. |
| [Resource List](actions/resource-list.md) | GET | Retrieves lesson resources from FlexiFunnels. |
| [Search Courses](actions/search-courses.md) | GET | Searches courses in FlexiFunnels. |
| [Unlock Mark Complete](actions/unlock-mark-complete.md) | DELETE | Deletes a lesson completion mark in FlexiFunnels. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves the authenticated member profile from FlexiFunnels. |


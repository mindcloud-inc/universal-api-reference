# <img src="https://images.mindcloud.co/apps/icons/thinkific_1773159491536.png" alt="Thinkific logo" width="28" height="28"> Thinkific: Universal API

Manage Thinkific courses, users, enrollments, and commerce data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/thinkific/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.thinkific.com
- **Vendor API docs:** https://developers.thinkific.com/api/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Course

| Action | Method | Description |
| --- | --- | --- |
| [Get Course](actions/get-course.md) | GET | Retrieves a course record from Thinkific. |
| [List Courses](actions/list-courses.md) | GET | Retrieves course records from Thinkific. |

### Course Review

| Action | Method | Description |
| --- | --- | --- |
| [Create Course Review](actions/create-course-review.md) | POST | Creates a new course review in Thinkific. |
| [List Course Reviews](actions/list-course-reviews.md) | GET | Retrieves course review records from Thinkific. |

### Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Create Enrollment](actions/create-enrollment.md) | POST | Creates a new enrollment in Thinkific. |
| [Get Enrollment](actions/get-enrollment.md) | GET | Retrieves an enrollment record from Thinkific. |
| [List Enrollments](actions/list-enrollments.md) | GET | Retrieves enrollment records from Thinkific. |
| [Update Enrollment](actions/update-enrollment.md) | PUT | Updates an existing enrollment in Thinkific. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Thinkific. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group record from Thinkific. |
| [List Groups](actions/list-groups.md) | GET | Retrieves group records from Thinkific. |

### Instructor

| Action | Method | Description |
| --- | --- | --- |
| [Create Instructor](actions/create-instructor.md) | POST | Creates a new instructor in Thinkific. |
| [Get Instructor](actions/get-instructor.md) | GET | Retrieves an instructor record from Thinkific. |
| [List Instructors](actions/list-instructors.md) | GET | Retrieves instructor records from Thinkific. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order record from Thinkific. |
| [List Orders](actions/list-orders.md) | GET | Retrieves order records from Thinkific. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product record from Thinkific. |
| [List Products](actions/list-products.md) | GET | Retrieves product records from Thinkific. |

### Site Script

| Action | Method | Description |
| --- | --- | --- |
| [Create Site Script](actions/create-site-script.md) | POST | Creates a new site script in Thinkific. |
| [List Site Scripts](actions/list-site-scripts.md) | GET | Retrieves site script records from Thinkific. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Thinkific. |
| [Get User](actions/get-user.md) | GET | Retrieves a user record from Thinkific. |
| [List Users](actions/list-users.md) | GET | Retrieves user records from Thinkific. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Thinkific. |


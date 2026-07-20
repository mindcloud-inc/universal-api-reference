# Remove Course from Branch with TalentLMS

Removes a course from a branch in TalentLMS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/branch-courses`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [Remove Course from Branch](https://documenter.getpostman.com/view/31867199/2sAY548Kou#remove-course-from-branch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch_id` | body | `list` | yes | Numeric branch ID. |
| `course_id` | body | `number` | yes | Numeric course ID. |

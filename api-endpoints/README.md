<!-- @format -->

### Api Endpoints for Blog Management

---

Authentication
| Method | URI |Auth| Description |
| -------- | ---- | ----- | ---- |
| `POST` | `/api/v1/auth/register` | public| users can register an account with required info passed from request body|
| `POST` | `/api/v1/auth/login` | public| users and admins can login with valid credentials|

---

User Management by Admin
| Method | URI | Auth |Description |
| -------- | ---- | ---- | ---- |
| `POST` | `/api/v1/users` | Private | admin can create a new user|
| `PUT` | `/api/v1/users/:userId` | Private | admin can update a user |
| `DELETE` | `/api/v1/users/:userId` | Private | admin can delete a user |
| `GET` | `/api/v1/users?limit=50` | Private | admin can see a list of users and can pass limit query parameter|
| `GET` | `/api/v1/users/:userId` | Private | admin can see a single user profile|

---

Profile Management by User
| Method | URI | Auth | Description |
| -------- | ---- | ---- | ---- |
| `GET` | `/api/v1/profile/:userId` | Public | user can view his own profile |
| `PATCH` | `/api/v1/profile/:userId` | Private | user can update his own profile |

---

Article Managment
| Method | URI | Auth | Description |
| -------- | ---- | ---- | ---- |
| `GET` | `/api/v1/articles?author=masud&limit=10&page=1` | Public | user can view their own and other user's posts and can pass query parameters (optional) |
| `POST` | `/api/v1/articles` | Privae | user can create a new article with title, content and optional cover photo |
| `PATCH` | `/api/v1/articles/:articleId` | Privae | user can update an article |
| `DELETE` | `/api/v1/articles/:articleId` | Privae | user can delete an article |

---

Comment Managment
| Method | URI | Auth | Description |
| -------- | ---- | ---- | ---- |
| `GET` | `/api/v1/comments?articleId=123&limit=10&page=1` | Public | user can view their own and other user's comments and can pass query parameters (optional) |
| `POST` | `/api/v1/comments?articleId=123` | Privae | user can post a new comment |
| `PATCH` | `/api/v1/comments/:commentId` | Privae | user can update a comment |
| `DELETE` | `/api/v1/commnets/:commentId` | Privae | user can delete a comment |

---

Cover photo upload
| Method | URI | Auth | Description |
| -------- | ---- | ---- | ---- |
| `POST` | `/api/v1/cover-photo` | Privae | user can upload a new cover photo |
| `PATCH` | `/api/v1/cover-photo/:photoId` | Privae | user can update the cover photo |
| `DELETE` | `/api/v1/cover-photo/:photoId` | Privae | user can delete the cover photo |

# IAM Lab

Hands-on Identity and Access Management (IAM) lab. This repo shows my progress through the lab with screenshots of each step.

## Progress

Screenshots are stored in [`screenshots/`](screenshots/) and listed here in order.

| # | Step | Screenshot |
|---|------|------------|
| 1 | **Explore IAM users** — The IAM console lists 4 users. `awsstudent` (path `/`) is the lab login, and its details show "Access denied" because it can't view itself. `user-1`, `user-2` and `user-3` are under path `/spl66/`. Each has 0 groups, a 6-minute-old password and an active access key. | ![IAM users](screenshots/01-iam-users.png) |
| 2 | **Add user-1 to the S3-Support group** — On `user-1`, choose "Add user to groups". Of the three groups, select `S3-Support` (it has `AmazonS3ReadOnlyAccess`). The other two are `EC2-Support` (`AmazonEC2ReadOnlyAccess`) and `EC2-Admin` (no managed policy). | ![Add user-1 to S3-Support](screenshots/02-add-user-1-to-s3-support.png) |
| 3 | **Confirm the group membership** — A banner says "User added to group S3-Support". On the `user-1` summary, the Groups tab lists `S3-Support` with `AmazonS3ReadOnlyAccess`, so `user-1` now has read-only access to S3 through the group. | ![user-1 in S3-Support](screenshots/03-user-1-in-s3-support.png) |
| 4 | **Add user-2 to the EC2-Support group** — On `user-2`, choose "Add user to groups" and select `EC2-Support`. This gives `user-2` read-only access to EC2 (`AmazonEC2ReadOnlyAccess`). | ![Add user-2 to EC2-Support](screenshots/04-add-user-2-to-ec2-support.png) |
| 5 | **Confirm the group membership** — A banner says "User added to group EC2-Support". On the `user-2` summary, the Groups tab lists `EC2-Support` with `AmazonEC2ReadOnlyAccess`. | ![user-2 in EC2-Support](screenshots/05-user-2-in-ec2-support.png) |

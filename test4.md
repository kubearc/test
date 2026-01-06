PRACTICAL TEST 
---

##  SECTION A: RHCSA (RHEL 9) – 30 MARKS

### Task A1: User, Group & Password Policy (10 Marks)
1. Create a group named `developers`
2. Create a user `appuser`
3. Configure:
   - Home directory: `/home/appuser`
   - Shell: `/bin/bash`
4. Add `appuser` to `developers`
5. Set password expiry to **60 days**

---

### Task A2: Permissions & Special Bits (10 Marks)
1. Create directory `/srv/apps`
2. Set:
   - Owner: `appuser`
   - Group: `developers`
3. Permissions:
   - Owner: full
   - Group: read/write
   - Others: no access
4. Apply **SGID** on the directory
5. Verify new files inherit group ownership

---

### Task A3: Storage & Mount (10 Marks)
1. Create a logical volume named `lv_apps` of size **600MB**
2. Format it with `xfs`
3. Mount it at `/apps`
4. Ensure the mount persists after reboot

---

##  SECTION B: AWS – 20 MARKS

### Task B1: EC2 & Security Group
1. Launch an EC2 instance:
   - Amazon Linux 2
   - Instance type: `t2.micro`
2. Create a Security Group:
   - Allow SSH (22) from your public IP only
   - Allow HTTP (80) from anywhere
3. Attach the Security Group to the instance
4. Verify SSH access

---

##  SECTION C: TERRAFORM – 20 MARKS

### Task C1: Terraform AWS Resource
1. Write Terraform configuration to:
   - Create an S3 bucket
2. Use variables for:
   - Bucket name
   - AWS region
3. Enable versioning on the bucket
4. Output the bucket name
5. Execute:
   ```bash
   terraform init
   terraform validate
   terraform apply
   ```
   
##  SECTION D: GIT & GITHUB – 15 MARKS

### Task D1: Git Workflow
1. Initialize a Git repository named `cloud-storage-lab`
2. Add Terraform configuration files to the repository
3. Commit the changes with the message: `Add S3 terraform configuration`
4. 4. Create a branch named `dev`
5. Modify the `README.md` file
6. Commit the changes
7. Merge the `dev` branch into the `main` branch
8. Push the repository to GitHub

---

##  SECTION E: CONTAINERS (PODMAN / DOCKER) – 15 MARKS

### Task E1: Web Container Deployment
1. Pull the `nginx` image using **Podman**
2. Run a container with the following configuration:
- **Container Name:** `web-app`
- **Port Mapping:** `8085:80`
3. Configure the container to restart automatically on system reboot
4. Verify container access using:
```bash
curl http://localhost:8085
```
   

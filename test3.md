# 🧪 PRACTICAL TEST 
---

## Platforms Covered
- Red Hat RHEL 9 (RHCSA)
- Amazon Web Services (AWS)
- HashiCorp Terraform
- Git & GitHub
- Podman / Docker

---

##  SECTION A: RHCSA (RHEL 9) – 25 MARKS

### Task A1: User & Directory Management 
1. Create a group named `build`
2. Create a user `runner`
3. Configure:
   - Home directory: `/opt/runner`
   - Shell: `/bin/bash`
4. Add `runner` to the `build` group
5. Create directory `/opt/builds` with:
   - Owner: `runner`
   - Group: `build`
   - Permissions: Owner full, Group read/write, Others none

---

### Task A2: ACL & Permissions 
1. Configure **default ACL** on `/opt/builds`
2. Ensure new files inherit:
   - Group write permission
3. Verify ACL configuration

---

### Task A3: Storage 
1. Create a logical volume named `lv_ci` of size **350MB**
2. Format it with `xfs`
3. Mount it permanently at `/ci-data`

---

##  SECTION B: AWS 

### Task B1: EC2 & Storage
1. Launch an EC2 instance:
   - Amazon Linux 2
   - Instance type: `t2.micro`
2. Create a **4 GB EBS volume**
3. Attach it to the EC2 instance
4. Mount it at `/data`
5. Ensure the mount persists after reboot

---

##  SECTION C: TERRAFORM 

### Task C1: Terraform Local Resource
1. Write Terraform configuration to:
   - Create a local file named `terraform-info.txt`
2. File must contain:
   - Your name
   - Current date
3. Apply Terraform configuration
4. Verify file creation

---

##  SECTION D: GIT & GITHUB 

### Task D1: Git Repository
1. Initialize a Git repository named `cron-git-lab`
2. Add the file `terraform-info.txt`
3. Commit with message: `Add terraform info file`
4. Push the repository to GitHub

---

##  SECTION E: CONTAINERS (PODMAN / DOCKER)

### Task F1: Container with Restart Policy

1. Pull the `busybox` image using **Podman**
2. Run a container with the following configuration:
   - **Container Name:** `cron-test`
   - **Command:**
     ```
     sh -c "while true; do date; sleep 30; done"
     ```
3. Configure the container to restart automatically on system reboot
4. Verify that the container is running successfully


# aws-linux-devops-ccna-lab-notes
this is the notes of all the courses I have learned
# AWS, Linux, DevOps & CCNA Practical Lab Notes

This repository contains my hands-on lab notes, command references, and practical setup workflows covering **AWS cloud infrastructure**, **Linux administration**, **enterprise networking (CCNA coursework)**, and **DevOps tooling (Jenkins, Docker, Ansible, Terraform)**.

---

## 1. Automated Website Deployment with Jenkins & AWS EC2

### What I Practiced
* Launched an **Amazon Linux 2023 EC2** instance and configured **Security Group** inbound rules (`SSH` port 22, `HTTP` port 80, and `Jenkins` port 8080).
* Installed and started **Jenkins** and a web server (`httpd` / `nginx`) on the Linux instance.
* Connected **GitHub** to Jenkins to pull source files and automate deploying a static web page onto the EC2 instance.

### Key Workflow Steps
1. Launch EC2 instance with a key pair (`.pem`) and restrict SSH access.
2. Update system packages and install Java, Git, Jenkins, and the web server (`dnf`).
3. Unlock Jenkins using the initial admin password and configure the GitHub repository URL in a Jenkins job.
4. Copy the pulled site files to the web root directory (`/var/www/html/`) and verify the live page via the EC2 public IP.

---

## 2. Linux Administration & Encryption Practice

### What I Practiced
* **Navigation & File Operations:** `pwd`, `ls -la`, `cd`, `mkdir`, `cp`, `mv`, `rm`, `cat`, `grep`, `find`
* **Permissions & Ownership:** Managing read/write/execute permissions and ownership using `chmod`, `chown`, and user/group commands (`useradd`, `passwd`, `sudo`).
  
* **Encryption & SSH Basics:** Generating SSH key pairs (`ssh-keygen`) for passwordless instance login and practicing file encryption/decryption workflows using `gpg`.

---

## 3. AWS Cloud Infrastructure Labs

### Core Services Practiced
* **Compute & Scaling:** Launched **EC2** instances, created **Launch Templates**, and tested **Auto Scaling Groups (ASG)** behind an **Application Load Balancer (ALB)**.
* **Networking & Security:** Configured custom **VPCs**, public/private **Subnets**, **Route Tables**, **Internet Gateways**, **Security Groups**, and **IAM** users, roles, and policies.
* **Storage & Content Delivery:** Created **S3** buckets, attached and formatted **EBS volumes**, created **EBS Snapshots**, and tested **CloudFront** distributions.

---

## 4. Enterprise Networking & CCNA Coursework Labs

### Switching & Layer 2 Segmentation
* **VLANs & Trunking:** Practiced segmenting broadcast domains across switches using Virtual LANs.
* **Spanning Tree Protocol (STP):** Studied Layer 2 loop prevention and root bridge election across redundant switch links.

### IPv4 Routing & Traffic Filtering
* **IPv4 Subnetting & Router Configuration:** Practiced CIDR subnetting, interface IP assignment, and static/default routing.
* **Dynamic Routing Protocols:** Configured **RIP**, **EIGRP**, and **OSPF** to understand route advertisement, metrics, and convergence.
* **Access Control Lists (ACLs):** Practiced standard and extended ACL rules to permit or deny traffic—concepts that translate directly to **AWS Security Groups** and **Network ACLs (NACLs)**.

---

## 5. DevOps Tooling Overview Labs

* **Docker:** Practiced pulling base images, building images from a `Dockerfile`, and running/inspecting containers (`docker build`, `docker run`, `docker ps`, `docker images`).
* **Ansible:** Practiced inventory setup and running basic playbooks to automate package installation and service configuration across Linux hosts.
* **Terraform:** Practiced writing basic `.tf` configuration files and running the core provisioning lifecycle (`terraform init`, `terraform plan`, `terraform apply`, `terraform destroy`).

---

*Note: All credentials, key pairs, and IP addresses are excluded from this repository.*

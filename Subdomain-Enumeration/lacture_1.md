# Introduction to Subdomain Enumeration 
### Subdomain
- It allows us to divide the website into smaller sections. with different duties.

### Subdomain Enumeration
- Find all subdomains associated with the main domain. and find loopholes that may have been overlooked

---

### Install assetfinder 
- Assetfinder: Use to find subdomains of the website.
```bash
sudo apt install assetfinder

assetfinder -subs-only tesla.com > sub-tesla.txt
# link.tesla.com 
```
- Find subdomain of `tesla.com` and keep output in file name `sub-tesla.txt` 

---

### Install httpx-toolkit
```bash
sudo apt install httpx-toolkit

cat sub-tesla.com | httpx-toolkit -title -p 443,8843 > new-sub-tesla.txt

cat new-sub-tesla.txt
# https://accounts.tesla.com []
```
- Verify the website name for each subdomain obtained through ports 443 and 8843 (ports often used for HTTPS).

---
✅ Day 4 Achievements**

1. **S3 Setup:** Created bucket `mayank-cloud-engineer-*******` with static website hosting + public access
2. **Content Upload:** Deployed `index.html` + `Resume.pdf` to S3 
3. **SSL Certificate:** Issued ACM cert for `mayankkemani.in` in `us-east-1` region
4. **CloudFront CDN:** Created distribution with S3 origin, HTTPS redirect, and Alternate Domain Names
5. **Domain Mapping:** Added CNAME record in GoDaddy pointing `mayankkemani.in` to CloudFront
6. **Bug Fix:** Resolved SSL error by using CloudFront URL instead of direct S3 link for resume
7. **Cache Management:** Learned and executed CloudFront invalidation `/*` to deploy updates

---

**💡 Key Learnings & Gotchas**

| Issue | Solution |
| --- | --- |
| **SSL Error on S3 link** | Never use `s3.amazonaws.com` URL. Always route via CloudFront |
| **Updates not reflecting** | CloudFront caches aggressively. Run invalidation `/*` after S3 changes |
| **ACM Cert not showing** | Cert MUST be in `us-east-1` for CloudFront to use it |
| **Resume 404 Error** | File name in `href` must exactly match S3 object key: `Resume.pdf` |

---

### **🚀 How to Deploy Updates**

1. Upload new `index.html` to S3 → Overwrite existing
2. CloudFront → Distributions → Invalidations → Create `/*`
3. Wait 2-3 mins → Hard refresh `Ctrl + Shift + R`

   
### **📞 Connect With Me**

**Mayank Kemani** | Cloud Engineer  
**Portfolio:** https://mayankkemani.in  
**LinkedIn:** https://www.linkedin.com/in/mayank-kemani-8a4693342/

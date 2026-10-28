# FestPass Assessment

## 1. Personal Details

- **Name:** Nitin Tripathi
- **REGNO:** 202401100100169
- **PORT:** 8069
- **Docker Hub Username:** `nitintripathi01`
- **Docker Hub Repository:** `https://hub.docker.com/repository/docker/nitintripathi01/fest-backend/general`

## 2. AI Tools Used

- **Gemini:** Used to generate the Dockerfile, `compose.yaml`, and terminal commands, and to troubleshoot path and build errors.

## 3. Docker Hub Digest

- **Image Version:** `1.0.0`
- **Digest:** `sha256:57aca93a0d27c04880e42a32c960d24a97cae5cf4a96fc67fa7d2e3abfc0c82e`

## 4. Vulnerability Before-and-After Comparison

Trivy was used to scan the Docker images before and after the image optimization and dependency updates.

| Image | Critical | High | Medium | Low | Unknown | Total Vulnerabilities | Image Size |
|---|---:|---:|---:|---:|---:|---:|---:|
| `fest-backend:0.1` | 234 | 2,243 | 7,514 | 3,206 | 158 | 13,355 | 401 MB |
| `fest-backend:0.2` | 0 | 44 | 58 | 61 | 1 | 164 | 54.7 MB |

### Key Improvements

- **Total vulnerabilities reduced by 98.77%**, from 13,355 to 164.
- **Critical vulnerabilities reduced by 100%**, from 234 to 0.
- **High-severity vulnerabilities reduced by 98.04%**, from 2,243 to 44.
- **Image size reduced by approximately 86.36%**, from 401 MB to 54.7 MB.
- The base operating system changed from Debian 13.1 to Debian 13.7.
- The Python runtime changed from Python 3.9 to Python 3.11.

### Security Scan Results

The updated image demonstrates a substantial reduction in reported vulnerabilities. However, the latest Trivy scan still identifies 44 high-severity vulnerabilities, along with medium-, low-, and unknown-severity findings. Further remediation and another security scan are recommended before considering the image production-ready.

**Reports:**
- Before: `reports/trivy-before.txt`
- After: `reports/trivy-after.txt`

## 5. Uncompleted Steps

`None`


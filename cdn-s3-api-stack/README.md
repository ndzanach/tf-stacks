# Edge-Services

Infrastructure for public-facing services powering content delivery, API backend, and DNS management.

## Components

- AWS S3 — Static asset storage (CDN origin)  
- AWS Lambda — API backend functions  
- AWS CloudFront — CDN for global delivery  
- AWS Route53 — DNS management  
- AWS ACM (Cert Manager) — SSL/TLS Certificates  
- AWS DynamoDB — Data storage  

## Usage

```bash
# Plan infrastructure changes
terraform plan -var-file="dev.tfvars"

# Apply infrastructure
terraform apply -var-file="dev.tfvars"

# Destroy infrastructure
terraform destroy -var-file="dev.tfvars"
```

## Structure

```
edge-services/
│
├── s3/              # Static assets bucket
├── lambda/          # Backend functions
├── cloudfront/      # CDN configuration
├── route53/         # DNS records
├── dynamodb/        # Data storage tables
├── cert-manager/    # SSL certificates
└── main.tf          # Root module
```

## Notes
- Environment configs via `dev.tfvars`, `prod.tfvars`  
- Built with Terraform  
- AWS Region: `af-south-1`





# Disclaimer

All code provided in all Git repositories is made available **"as is"** without any warranty of any kind, express or implied, including, but not limited to, warranties of merchantability, fitness for a particular purpose, or non-infringement. The author(s) of this code shall not be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of the code in these repositories, even if advised of the possibility of such damage.

**Use any code from these repositories at your own risk.**
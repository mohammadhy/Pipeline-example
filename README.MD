How Have Code Signing
- gpg --full-generate-key
- gpg --armor --export <Your-Key-ID>
- git config --global user.signingkey <Your-Key-ID>
- git config --global commit.gpgsign true

### use Trivy Local DB
 docker run --rm -v $PWD:/app -v /var/run/docker.sock:/var/run/docker.sock 192.168.42.3:5000/aquasec/trivy:0.58.0 image --db-repository $REGISTERY/aquasecurity/trivy-db:2 --java-db-repository $REGISTERY/aquasecurity/trivy-java-db:1 -f json -o /app/trivy.json  $REGISTERY/$IMAGE:$CI_COMMIT_SHORT_SHA'''

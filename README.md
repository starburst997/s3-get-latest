# s3-get-latest

Download all the files from the latest version folder in S3

**Works only on linux runner** (maybe macos as well).

## Secrets:

TODO: How to get access key in AWS... Simple guide.

## Usage:

```yml
- name: Download all files in the latest version folder
  uses: starburst997/s3-get-latest@v1
  with:
    key-id: ${{ secrets.S3_KEY_ID }}
    secret-access-key: ${{ secrets.S3_SECRET_ACCESS_KEY }}
    region: ${{ secrets.S3_REGION }}
    endpoint: ${{ secrets.S3_ENDPOINT }}
    bucket: ${{ secrets.S3_BUCKET }}

    dst-dir: 'folder/to/download/to'
    src-dir: 'apps/test/internal/windows'
    release: '5'
```
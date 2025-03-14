# alpine-base

<!---
Note: Do NOT edit directly, this file was generated using https://github.com/chainguard-images/readme-generator
-->

[![CI status](https://github.com/chainguard-images/alpine-base/actions/workflows/release.yaml/badge.svg)](https://github.com/chainguard-images/alpine-base/actions/workflows/release.yaml)

Alpine base image built with [apko](https://github.com/chainguard-dev/apko). Uses packages from the [Alpine distribution](https://www.alpinelinux.org/).

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/alpine-base:latest
```

## Supported tags

| Tag | Digest | Arch |
| --- | ------ | ---- |
| `latest` | `sha256:caededb20fe692c948a7ea1ba88d732aae1256d5ab3f35a188d756a96e57fd89`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:caededb20fe692c948a7ea1ba88d732aae1256d5ab3f35a188d756a96e57fd89) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |


## Usage

```
docker run cgr.dev/chainguard/alpine-base echo "hello"
```

See the [examples/](./examples/) directory for how
to use this as a base image.


## Signing

All Chainguard Images are signed using [Sigstore](https://sigstore.dev)!

<details>
<br/>
To verify the image, download <a href="https://github.com/sigstore/cosign">cosign</a> and run:

```
COSIGN_EXPERIMENTAL=1 cosign verify cgr.dev/chainguard/alpine-base:latest | jq
```

Output:
```
Verification for cgr.dev/chainguard/alpine-base:latest --
The following checks were performed on each of these signatures:
  - The cosign claims were validated
  - Existence of the claims in the transparency log was verified offline
  - Any certificates were verified against the Fulcio roots.
[
  {
    "critical": {
      "identity": {
        "docker-reference": "ghcr.io/chainguard-images/alpine-base"
      },
      "image": {
        "docker-manifest-digest": "sha256:caededb20fe692c948a7ea1ba88d732aae1256d5ab3f35a188d756a96e57fd89"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "6c45f1b1dc86cf06887bb6e7b8887a3d737f321d",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/alpine-base",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEYCIQCvBLp2gtZX7Aw8/WpNRO/9oRYJozi7PAuf5QrvJrZ2rwIhAMRzCVpJy1RUVXSCVZ4lrIWZOvnlsaC6d++anAntqbaO",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiJhZTQ0NTMwYWE3NGNhNzY1Mzk1M2YxMDE2YTJhMDhjZjVkNWRjZDA2OTdiOGZhODhhMTE3YzJiYzdkODFmZmE2In19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJUUNBK2xqMmU4YlZXNStMZExHanI4Ny90ZWpPU25CcmtROEgzOGpHczRRKytRSWdZb1lCL0RnVUVzRTJrNHFUNkNZc0hscU9oQjg5bzVNcyt5SkJCejAzMW9ZPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUjBSRU5EUVhweFowRjNTVUpCWjBsVlIzTk9hRWR1ZFhsUGNWSkpVbXRCYWpSQlVXUkVlbEp1VDJsamQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFFU1hkTlJFVjRUa1JSZDFkb1kwNU5ha2w0VFVSSmQwMUVSWGxPUkZGM1YycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZPSzBJMlYyVlVaMWxRWm10blRVMDVla2d4VVhKWFdsRkhiVzlaZG5GU05EaGlVWFlLZDFwMk9XUkVZVXRaZVVwd1ZERXdNMmRyZUVabFJXdEpiQ3REYjBwRmJ6Rk1kakpUZERkSVNFTmlkbkptZFhGVVkyRlBRMEZzYTNkblowcFdUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlUwY0hkSUNtVnNiR2xQWTFsTGQyNUVZM2xIUzJoVU0yVndaRGRqZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJKUldVUldVakJTUVZGSUwwSkhUWGRaV1ZwbVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5Um5OalIyeDFXbE14YVZsWVRteE1lVFZ1WVZoU2IyUlhTWFprTWpsNVlUSmFjMkl6WkhwTU0wcHNZa2RXYUdNeVZYVmxWMFowQ21KRlFubGFWMXA2VERKb2JGbFhVbnBNTWpGb1lWYzBkMDlSV1V0TGQxbENRa0ZIUkhaNlFVSkJVVkZ5WVVoU01HTklUVFpNZVRrd1lqSjBiR0pwTldnS1dUTlNjR0l5TlhwTWJXUndaRWRvTVZsdVZucGFXRXBxWWpJMU1GcFhOVEJNYlU1MllsUkJWMEpuYjNKQ1owVkZRVmxQTDAxQlJVTkNRV2g2V1RKb2JBcGFTRlp6V2xSQk1rSm5iM0pDWjBWRlFWbFBMMDFCUlVSQ1EyY3lXWHBSTVZwcVJtbE5WMUpxVDBSYWFscHFRVEpQUkdjeldXMUpNbHBVWkdsUFJHYzBDazR5UlhwYVJHTjZUakpaZWsxcVJtdE5RbmRIUTJselIwRlJVVUpuTnpoM1FWRlJSVVJyVG5sYVYwWXdXbE5DVTFwWGVHeFpXRTVzVFVOelIwTnBjMGNLUVZGUlFtYzNPSGRCVVZWRlNGZE9iMWxYYkhWYU0xWm9ZMjFSZEdGWE1XaGFNbFo2VERKR2MyTkhiSFZhVXpGcFdWaE9iRTFDTUVkRGFYTkhRVkZSUWdwbk56aDNRVkZaUlVRelNteGFiazEyWVVkV2FGcElUWFppVjBad1ltcERRbWxSV1V0TGQxbENRa0ZJVjJWUlNVVkJaMUkzUWtoclFXUjNRakZCUVdobkNtdDJRVzlWZGpsdlVtUklVbUY1WlVWdVJWWnVSMHQzVjFCalRUUXdiVE50ZGtOSlIwNXRPWGxCUVVGQ1p5OU1NRFkyWTBGQlFWRkVRVVZaZDFKQlNXY0tTRE13Wms1UVNIUkpXbVptVFV0VVZIbENRakZMVVhscGVDOVdNVUZKYkdwalkyTkRjMU52TDJoTFJVTkpSMmh0V2tGSVdEQlBUbHBKVDJoUVRXNUZWZ3B3UTJFcmJreEdUSHB1TkZsdFZUaHBTbEVyUWxVMmJWTk5RVzlIUTBOeFIxTk5ORGxDUVUxRVFUSm5RVTFIVlVOTlFtc3JjV00wZW10M01sWTBURVI2Q21WdlZqZHVkVFY1WlZsMlJ6UTFWbll2YmxaTGExUkhVME5EUjBJMFYwNU5VbGxYZUhNMEswMUZVRzR4VFRSVFpVRkJTWGhCU1hKelkyNHpWbXRNYmpZS2R6Sk5ZbmhQU0cxUWFHWkNRVkJxYUdWb2NVMVNTVXhaT1RGelUzTXlUME5TYjBoVFJWZ3JkRGhPY1UwMU5qUjZVM1JSYWxoUlBUMEtMUzB0TFMxRlRrUWdRMFZTVkVsR1NVTkJWRVV0TFMwdExRbz0ifX19fQ==",
          "integratedTime": 1666228521,
          "logIndex": 5465923,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/alpine-base/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/alpine-base",
      "githubWorkflowSha": "6c45f1b1dc86cf06887bb6e7b8887a3d737f321d",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3286122832",
      "sha": "6c45f1b1dc86cf06887bb6e7b8887a3d737f321d"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).


# android_device_qcom_sepolicy-legacy

The legacy Qualcomm SELinux policy tree — `device/qcom/sepolicy-legacy` — recovered from
[Software Heritage](https://archive.softwareheritage.org/) and re-hosted so it cannot be lost again.

Upstream was `TipzTeam/android_device_qcom_sepolicy-legacy` (branch `lineage-19.0`), which no longer
exists. LineageOS dropped the older Qualcomm platforms after 18.1, and a device tree that still
references this policy fails with:

```
device/nextbit/ether/BoardConfig.mk: device/qcom/sepolicy-legacy/sepolicy.mk: No such file
```

Apache-2.0 source only: SELinux policy, makefiles and XML. **No binaries, no proprietary blobs.**

## Platforms covered

`apq8084` `msm8226` `msm8909` `msm8916` `msm8952` `msm8960` `msm8974` `msm8976` `msm8992` `msm8994`
plus `common`, `legacy-common`, `private`, `public`, `ssg` and `test`.

Useful to any device on those SoCs whose LineageOS support was removed — not just the one that
prompted the recovery.

## Use

Add it to a local manifest; the repo root *is* the policy tree, so it maps directly:

```xml
<project name="TheDBP/android_device_qcom_sepolicy-legacy"
         path="device/qcom/sepolicy-legacy" remote="github" revision="main" />
```

## Provenance

Recovered while porting the Nextbit Robin (`ether`, msm8992) past LineageOS 18.1 — see
[ether-robin-lineage](https://github.com/TheDBP/ether-robin-lineage). Content is unmodified from the
recovered upstream.

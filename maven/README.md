# Maven

Contains Maven repository fixtures.

## Structure

Fixtures follow the standard Maven repository layout:
`{groupId_path}/{artifactId}/{version}/{groupId}.{artifactId}.{version}.{ext}`

Release qualifiers are embedded in the version string (e.g. `1.0.0.release-00001`),
matching the pattern `[a-zA-Z]+-\d+`.

## Packages

### com.example.fixture / raccoon

| Version | Release |
|---------|---------|
| 1.0.0.rhlw-00001 | rhlw-00001 |
| 1.0.0.rhlw-00002 | rhlw-00002 |
| 2.0.0.rhlw-00001 | rhlw-00001 |

### blissed / blissed

| Version | Release |
|---------|---------|
| 1.0-beta-3 | — |
| 1.0-beta-3.rhlw-00001 | rhlw-00001 |
| 1.0-beta-3.rhlw-00002 | rhlw-00002 |

### org.yaml / snakeyaml

| Version | Release |
|---------|---------|
| 1.33 | — |
| 1.33.rhlw-00001 | rhlw-00001 |

## How to add a new fixture

1. Create the version directory: `{groupId_path}/{artifactId}/{version}/`
2. Add a `.pom` file: minimal Maven POM with groupId, artifactId, and version
3. Add a `.jar` file: a valid ZIP archive containing `META-INF/MANIFEST.MF`
4. Update this README

### Creating a minimal JAR

```bash
mkdir -p META-INF
printf 'Manifest-Version: 1.0\n' > META-INF/MANIFEST.MF
zip -q output.jar META-INF/MANIFEST.MF
```

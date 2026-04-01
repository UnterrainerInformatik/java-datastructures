# Log4j Migration Plan: datastructures

**Layer**: 1 — update after `parent-pom`.

## Before Starting

Prompt the user for the following version numbers before making any changes:

| Variable | Question |
|----------|----------|
| `NEW_PARENT_POM_VERSION` | What is the new `parent-pom` version? |
| `OWN_NEW_VERSION` | What version should `datastructures` be bumped to? (currently `1.0.0`) |

## Context

Part of a migration from Log4j 1.x to Log4j 2.25.3 across all libraries. The logging backend change happens in `parent-pom`; this project just needs the parent version bump. This library has no logging config files and no `@Slf4j` usage.

## Current State

- **Artifact**: `info.unterrainer.commons:datastructures`
- **Parent**: `parent-pom:1.0.1`
- **Own dependencies**: none
- **log4j.properties**: none
- **@Slf4j usage**: none

## Steps

### 1. Update parent version in `pom.xml`

Change the parent version (line 8) to the new parent-pom version:

```xml
<parent>
    <groupId>info.unterrainer.commons</groupId>
    <artifactId>parent-pom</artifactId>
    <version>NEW_PARENT_POM_VERSION</version>
</parent>
```

### 2. Bump own version

Increment `<version>` (line 13, currently `1.0.0`).

### 3. Build, test, install

```bash
mvn clean install
```

### 4. Verify logging deps

```bash
mvn dependency:tree -Dincludes="*log4j*,*slf4j*"
```

Must show Log4j 2 artifacts, not `slf4j-log4j12` / `slf4j-simple`.

## Files Changed

| File | Action |
|------|--------|
| `pom.xml` | Update parent version, bump own version |

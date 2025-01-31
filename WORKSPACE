workspace(name = "gov_nist_metaschema_framework_js")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

local_repository(
    name = "com_google_j2cl",
    path = "../..",
)

load("@com_google_j2cl//build_defs:repository.bzl", "load_j2cl_repo_deps")
load_j2cl_repo_deps()

load("@com_google_j2cl//build_defs:workspace.bzl", "setup_j2cl_workspace")
setup_j2cl_workspace()

_MAVEN_CENTRAL_URLS = ["https://repo1.maven.org/maven2/"]


load("@com_google_j2cl//build_defs:rules.bzl", "j2cl_maven_import_external")

j2cl_maven_import_external(
    name = "org_checkerframework_checker_qual-j2cl",
    annotation_only = True,
    artifact = "org.checkerframework:checker-qual:2.5.3",
    artifact_sha256= "7be622bd25208ccfbb9b634af8bd37aef54368403a1fdce84d908078330a189d",
    server_urls = _MAVEN_CENTRAL_URLS,
)

j2cl_maven_import_external(
    name = "com_google_errorprone_error_prone_annotations-j2cl",
    annotation_only = True,
    artifact = "com.google.errorprone:error_prone_annotations:2.23.0",
    artifact_sha256= "ec6f39f068b6ff9ac323c68e28b9299f8c0a80ca512dccb1d4a70f40ac3ec054",
    server_urls = _MAVEN_CENTRAL_URLS,
)

j2cl_maven_import_external(
    name = "com_google_code_findbugs_jsr305-j2cl",
    annotation_only = True,
    artifact = "com.google.code.findbugs:jsr305:3.0.2",
    server_urls = _MAVEN_CENTRAL_URLS,
)

j2cl_maven_import_external(
    name = "com_google_j2objc_annotations-j2cl",
    annotation_only = True,
    artifact = "com.google.j2objc:j2objc-annotations:jar:1.3",
    artifact_sha256= "21af30c92267bd6122c0e0b4d20cccb6641a37eaf956c6540ec471d584e64a7b",
    server_urls = _MAVEN_CENTRAL_URLS,
)

j2cl_maven_import_external(
    name = "com_google_guava-j2cl",
    artifact = "com.google.guava:guava-gwt:32.1.1-jre",
    artifact_sha256= "5c6891832727c728a09e4e84bad83517db8bd50b435cd362aafa08ef99932d6b",
    server_urls = _MAVEN_CENTRAL_URLS,
    deps = [
        "@com_google_code_findbugs_jsr305-j2cl",
        "@com_google_errorprone_error_prone_annotations-j2cl",
        "@com_google_j2cl//:jsinterop-annotations-j2cl",
        "@com_google_j2objc_annotations-j2cl",
        "@org_checkerframework_checker_qual-j2cl",
    ],
)

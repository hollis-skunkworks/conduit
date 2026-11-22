# Conduit

Experimental standalone command runtime. Read README.md, CONTRIBUTING.md and SECURITY.md for architecture and the existing fail-closed policy, identity, approval, sandbox and redaction boundaries.

- Linux is the supported runtime platform.
- Run checks from this module root with GOWORK=off: go vet ./... and go test -race -count=1 ./.... CI also checks formatting, module consistency, transport boundaries, vulnerabilities, public hygiene and Caster integration.
- .github/workflows/build.yml gates artifact packaging on the full check job.
- Existing Go module identity and consumer pins are deferred until portfolio adoption; do not publish new module tags before that adoption.
- Source cleanup does not deploy, migrate data or restart live services. Keep running installations and operational credentials separate.

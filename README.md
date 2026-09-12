# Advanced Fabrics Provider SDK

Providers adapt implementation-specific network systems to the versioned contract in `advanced-fabrics/api/proto/provider/v1/provider.proto`.

A provider must advertise protocol version and capabilities before serving requests. `Observe` is the baseline capability. `Plan` may return a deterministic proposed diff. `Apply` is optional and must reject requests unless provider capability, AdvancedFabric policy, RBAC and workload identity all authorize mutation.

Provider implementations must not place credentials in observations, plans, status, logs or conformance results. Transport uses mutual TLS; the reference runtime uses cert-manager certificates and permits a replaceable SPIFFE identity provider.

Official provider registration requires Apache-2.0-compatible licensing, immutable releases, signatures, provenance, SBOMs and the provider conformance profile.
Provider SDK, registry and test doubles

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/7K-Inari/.github/main/profile/assets/icon-inari.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/7K-Inari/.github/main/profile/assets/icon-inari-light.svg">
    <img alt="Inari" src="https://raw.githubusercontent.com/7K-Inari/.github/main/profile/assets/icon-inari.svg" width="144">
  </picture>

# Inari

  **The platform control plane that builds its own catalog.**

  A multi-tenant Internal Developer Platform for Kubernetes and AWS.

  **Pre-v1 · Active development · Apache-2.0**
</div>

## Why Inari?

Inari is **the platform control plane that builds its own catalog**: agents discover the capabilities running in each cluster, so the catalog reflects reality rather than a manually maintained inventory. It belongs to the Internal Developer Platform and developer-control-plane category alongside Backstage, Port, and Cortex.

Inari is designed around tenant-aware APIs, outbound-only cluster agents, GitOps delivery, and a hub that holds no tenant kubeconfigs or cloud keys.

## Repository map

| Repository | Role |
| --- | --- |
| [inari-server](https://github.com/7K-Inari/inari-server) | Go control plane: API/BFF, tenancy, catalog, orchestration, fleet, policy, and audit. |
| [inari-agent](https://github.com/7K-Inari/inari-agent) | Per-cluster controller for outbound connectivity, capability discovery, and reconciliation. |
| [inari-ui](https://github.com/7K-Inari/inari-ui) | React console for developers and platform operators. |
| [inari-api](https://github.com/7K-Inari/inari-api) | Versioned protobuf and OpenAPI contracts shared by Inari components. |
| [inari-cli](https://github.com/7K-Inari/inari-cli) | Command-line interface for Inari workflows and automation. |
| [inari-plugin-sdk](https://github.com/7K-Inari/inari-plugin-sdk) | SDK for building Inari control-plane extensions. |
| [inari-ui-plugin-sdk](https://github.com/7K-Inari/inari-ui-plugin-sdk) | SDK for extending the Inari console with UI plugins. |
| [inari-catalog](https://github.com/7K-Inari/inari-catalog) | Curated KRO packages and reusable golden-path capabilities. |
| [inari-ext-argocd](https://github.com/7K-Inari/inari-ext-argocd) | Reference extension for Argo CD integration. |
| [inari-release-bundle](https://github.com/7K-Inari/inari-release-bundle) | Helm charts, day-0 bootstrap, deployment automation, and disaster-recovery assets. |
| [inari-docs](https://github.com/7K-Inari/inari-docs) | Architecture plan, ADRs, operator runbooks, tutorials, and threat model. |

## Quickstart: register → discover → deploy

Operators can start with the [day-0 bootstrap quickstart](https://github.com/7K-Inari/inari-release-bundle#quickstart-day-0-bootstrap). Then follow the golden path:

1. **Register** a cluster using the [cluster registration tutorial](https://github.com/7K-Inari/inari-docs/blob/main/docs/tutorials/register-a-cluster.md).
2. **Discover** the CRDs, operators, and other capabilities that the agent adds to the catalog automatically.
3. **Deploy** a curated package and follow its GitOps delivery and health in the [first-deploy tutorial](https://github.com/7K-Inari/inari-docs/blob/main/docs/tutorials/first-deploy.md).

> **3-minute demo — coming soon.** GP-2 is still pending; the register → discover → deploy demo video has not been published.

## Documentation

- [Architecture and platform plan](https://github.com/7K-Inari/inari-docs/blob/main/docs/architecture/inari-platform-plan.md)
- [Security threat model](https://github.com/7K-Inari/inari-docs/blob/main/docs/security/threat-model.md)
- [Backup and restore operator guide](https://github.com/7K-Inari/inari-docs/blob/main/docs/operator-guide/backup-restore.md)
- [High-availability operator guide](https://github.com/7K-Inari/inari-docs/blob/main/docs/operator-guide/high-availability.md)
- [Published documentation](https://docs.7kgroup.org/inari)

## License

Every project repository listed above uses [Apache License 2.0](https://github.com/7K-Inari/inari-docs/blob/main/LICENSE). Licensing was merged across all 11 active Inari project repositories on **2026-11-11**.

## Contributing

**External contributions are currently paused.** The canonical Harmony-based [ICLA](https://github.com/7K-Inari/inari-docs/blob/main/docs/legal/cla/icla.md) and [CCLA](https://github.com/7K-Inari/inari-docs/blob/main/docs/legal/cla/ccla.md) are drafts, and CLA Assistant is not yet activated. Contributions will open after the G1 gate is complete, including CLA activation. Read the [contribution guide](https://github.com/7K-Inari/.github/blob/main/CONTRIBUTING.md) and [CLA approval status](https://github.com/7K-Inari/inari-docs/blob/main/docs/legal/cla/README.md) for the authoritative current state. Do not email signed agreements or attach them to issues or pull requests.

**Upcoming click-through flow — not live:** after activation, a pull-request author will follow the CLA Assistant comment, authenticate with GitHub, review and accept the applicable individual or corporate agreement, and return to the pull request for a passing CLA status check. A DCO `Signed-off-by` line does not replace the CLA.

## Security

Please report suspected vulnerabilities privately and never through a public issue, discussion, or pull request. See the [security policy and disclosure process](https://github.com/7K-Inari/.github/blob/main/SECURITY.md).

Contact: [security@7kgroup.org](mailto:security@7kgroup.org). This mailbox is being set up under ORG-2; until ORG-2 confirms it is live, use the [7K Group contact page](https://7kgroup.org/contact) for initial private coordination without sensitive details.

## Status and design partners

Inari is **pre-v1 and under active development**; interfaces and operational guidance may change before v1. If you want to help shape the platform through a **paid design-partner program**, [talk to 7K Group](https://7kgroup.org).

# Product Analytics Instrumentation & Event Tracking Taxonomy 📊

This document establishes the official product analytics event logging taxonomy for our enterprise platform portal. Rather than relying on simple, uninformative page-view logs, this schema utilizes a strict **Object-Action** data model to capture precise developer behavioral signals. This telemetry directly empowers product teams to diagnose funnel conversion drops and measure true feature retention.

---

## 📐 The Object-Action Data Blueprint

Every analytical event sent to our product telemetry infrastructure must follow a rigid structure containing the specific user interface object, the action performed, and context-rich metadata properties.

### Event Logging Schema Matrix
| Event Name | Triggering User Action | Contextual Properties Captured | Primary Product Health Metric |
| :--- | :--- | :--- | :--- |
| `identity_token_request_initiated` | Developer clicks the "Generate Token" button. | `subaccount_region`, `auth_protocol`, `interface_mode` (UI vs CLI) | Funnel Activation Rate |
| `identity_token_request_completed` | The system successfully returns an access secret. | `duration_milliseconds`, `allocated_token_scope` | Time-to-First-Token (TTFT) Latency |
| `identity_token_request_failed` | System returns a security or network error payload. | `error_classification_code`, `network_origin_type` | Platform Friction Coefficient |
| `integration_template_shared` | Developer copies or exports an environment configuration. | `target_platform`, `template_size_lines` | User Referral / Virality Index |

---

## 💻 Analytics Implementation Payload (JSON Schema)

```json
{
  "analytics_event_payload": {
    "event_name": "identity_token_request_completed",
    "user_properties": {
      "user_id": "usr_90412",
      "organization_segment": "Enterprise_Premium",
      "historical_deployment_count": 42
    },
    "event_properties": {
      "duration_milliseconds": 185,
      "allocated_token_scope": "READ_WRITE",
      "deployment_success_flag": true
    },
    "system_environment": {
      "client_interface": "BTP_CLI_v2.6",
      "geographical_ingress_node": "AP-SOUTH"
    }
  }
}

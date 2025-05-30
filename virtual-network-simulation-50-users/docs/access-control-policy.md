# Access Control Policy

## Objective
To define how access to different parts of the virtual network is managed, ensuring security, role separation, and efficient operations in a simulated 50-user enterprise network.

---

## Role-Based Access Control (RBAC)

| Role             | Description                          | Access Level                               |
|------------------|--------------------------------------|--------------------------------------------|
| **Network Admin**| Responsible for full network config  | Full access to firewall, VPN, monitoring   |
| **IT Support**   | Manages users and logs               | Limited firewall access, full monitoring   |
| **Employee**     | Regular enterprise user              | Access to internal services and internet   |
| **Guest**        | Temporary access                     | Internet access only (isolated subnet)     |

---

## Subnet Access Matrix

| Subnet            | Admin | IT Support | Employee | Guest |
|-------------------|:-----:|:----------:|:--------:|:-----:|
| `10.0.0.0/24` – Admin/Infra     | ✅     | ✅         | ❌       | ❌     |
| `10.0.1.0/24` – Internal Users  | ✅     | ✅         | ✅       | ❌     |
| `10.0.2.0/24` – Guest Network   | ✅     | ✅         | ❌       | ✅     |
| Monitoring System (Zabbix/Nagios) | ✅   | ✅         | ❌       | ❌     |

---

## VPN Access Policy

- All users must authenticate via OpenVPN using individual credentials and MFA.
- Admin and IT Support roles receive full tunnel access.
- Employees have split tunnel access (limited internal reach).
- Guests are not permitted VPN access.

---

## Authentication

- Password + MFA (simulated)
- Certificates for OpenVPN users
- User profiles created using `create_users.sh` (see `/scripts`)

---

## Logging and Auditing

- All admin logins to pfSense and VPN are logged
- Firewall rule changes are tracked
- Zabbix/Nagios alerts log access anomalies

---

## Future Improvements
- Integrate LDAP or simulated Azure AD
- Role-based VPN profiles with group policies
- Automated user provisioning using Ansible
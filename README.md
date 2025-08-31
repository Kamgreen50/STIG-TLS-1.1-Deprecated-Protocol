# STIG – TLS Version 1.1 Deprecated Protocol (Plugin ID: 157288)

## Before
- Finding: TLSv1.1 is enabled on the system.
- Risk: Deprecated protocol, no longer supported by major browsers or vendors.
- Evidence:  
  - before-tenable-finding.png  

## Remediation
- Disable TLS 1.0 and TLS 1.1, leaving TLS 1.2 or higher enabled.
- Methods:  
  1. **Windows**: Use Registry Editor or Group Policy  
     - Path: `HKLM\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols`  
     - Set `Enabled=0` and `DisabledByDefault=1` for TLS 1.0/1.1.  
  2. **Linux**: Update OpenSSL / web server configs (Apache, Nginx) to require TLS 1.2+.  
- Tools: IIS Crypto (Windows), `openssl s_client` (Linux).  
- Verify: Re-scan with Tenable or test with SSL Labs.  

## After Remediation
(Placeholder – will add screenshot once fixed and rescanned)

- Confirm Tenable no longer reports plugin ID 157288.
- Proof: Updated Tenable scan screenshot (to be added).


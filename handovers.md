# End-of-shift handovers · Cloudora, Larkspur Home

## Cloudora · Shift 1 · 2026-09-14

Closed all four assigned incidents. CLD-0201 was resolved after reviewing the repeated failed sign-ins, CLD-0202 was closed after Defender successfully quarantined the PUA and a follow-up scan returned clean, and CLD-0203 was closed after the guest sign-in matched the user's established baseline and authorized contractor activity. CLD-0204 was closed as authorized vulnerability scanning under change record CHG-2101. No incidents remain open; continue monitoring for unusual authentication activity, guest accounts without MFA, endpoint threat reappearance, and scanner activity outside approved change windows.

## Cloudora · Shift 2 · 2026-09-23

Investigated and closed multiple alerts during the shift. CLD-0205 was confirmed as a phishing attempt targeting Marcus Joe; no credentials were entered and the malicious sender/domain and URL were addressed. CLD-0206 was closed as legitimate documented travel for Helen Dray, and CLD-0207 was closed as authorized scheduled marketing activity. CLD-0208 was closed as a duplicate of CLD-0205 after the gateway provided additional sandbox confirmation of the malicious URL. No incidents remain open from this shift; continue monitoring for additional deliveries or activity related to the phishing indicators.

## Cloudora · Shift 3 · 2026-09-24

Closed all four assigned incidents. CLD-0209 was escalated due to significant changes from the guest account’s established baseline and access to the Payroll-Mapping library. CLD-0210 was closed as a false positive after the service account lockout was tied to the approved CHG-2102 backup migration window. CLD-0211 was closed as a false positive after HD-5144 and proxy logs confirmed the 60-second connections to cdn-metrics.example were from the authorized Manchester monitoring-agent pilot. CLD-0212 was closed as a contained true positive after Conditional Access blocked attempts from a known CLD-0001 watchlist IOC before authentication. Continue monitoring the guest account investigation, service-account activity outside approved change windows, and further attempts from known watchlist infrastructure.

## Cloudora · Shift 4 · 2026-10-02

CLD-0213 was escalated after suspicious OAuth consent by the previously compromised ewalsh.ext account granted persistent mail and file access, followed by significant traffic to the Bexley Sync Utility infrastructure. CLD-0214 was confirmed as a DLP true positive after Marcus sent a payroll export containing sensitive salary data to a personal email address with no documented authorization, requiring follow-up on business justification and potential data exposure. CLD-0215 was closed as a false positive after HD-5150 confirmed the ransomware-pattern file was part of an approved security-awareness exercise. CLD-0216 was confirmed as attempted MFA fatigue against ops-admin; all pushes were denied with no successful access, but the password stage passed, so the next shift should watch for further authentication attempts, OAuth persistence, and additional sensitive-data movement.

## Cloudora · Shift 5 · 2026-10-05

CLD-0217 was escalated as S2/High after 41 MB was transferred from the payroll integration server to a young external domain that matched 0/3 characteristics of the legitimate Bexley feed. CLD-0218 and CLD-0219 were closed as false positives after confirming Omar’s documented recurring Dubai travel and Tara Kemp’s approved Payroll-Admins role change under CHG-2105. CLD-0220 was closed as a Low-severity true positive after confirming a subscription-bombing attack against the finance mailbox, with no related account compromise identified in the available evidence. The next shift should watch for further traffic to bexley-sync.example, additional unauthorized transfer activity, and any financial or security notifications that may have been concealed by the subscription flood.

## Cloudora · Shift 6 · 2026-10-06

All four tickets were closed this shift. CLD-0221, CLD-0222, and CLD-0223 involved related suspicious activity from IP 192.0.2.146, including malicious inbox forwarding, internal phishing from a compromised guest account, and suspected session token replay. CLD-0224 was a routine antivirus digest with three successfully remediated detections and no active threats. The next shift should verify containment of the affected accounts, confirm removal of the malicious forwarding rule and revocation of suspicious sessions, and monitor for additional activity involving 192.0.2.146 and the phishing destination 192.0.2.203.

## Cloudora · Shift 7 · 2026-10-12

All four Shift 7 tickets were closed. CLD-0226 confirmed malicious scheduled-task persistence on LDN-SRV-APP1; the proxy blocked subsequent polls, but the incident response team must verify removal of BexleySyncHealth and review the integration service account. CLD-0225 confirmed Conditional Access blocked the observed authentication attempts from 192.0.2.146 and 192.0.2.203, while CLD-0227 was verified as legitimate Bexley correspondence and CLD-0228's elevated identity alert volume was consistent with previously documented compromise activity. The next shift should confirm scheduled-task eradication, monitor for renewed activity from suspicious infrastructure, and investigate any identity alerts not explained by existing incidents.

## Cloudora · Shift 8 · 2026-10-13

Completed investigations for CLD-0229, CLD-0230, CLD-0231, and CLD-0232. CLD-0229 involved Bexley Payroll breach indicators and related suspicious activity requiring continued monitoring. CLD-0230 was determined to be a false positive after confirming the outbound SFTP transfer matched approved change CHG-2110. CLD-0231 identified continued refresh-token use after Marcus's password reset, requiring verification of session revocation. CLD-0232 identified a suspicious inbox rule hiding invoice emails, requiring rule removal, mailbox review, and confirmation of remediation. The next shift should prioritize follow-up on Marcus's account security and mailbox remediation.

## Cloudora · Shift 9 · 2026-10-14

Closed CLD-0233 through CLD-0236 after reviewing the available evidence. CLD-0233 was associated with the documented payroll cutover, while CLD-0234 identified excessive permissions granted to the Cloudora Payroll Bridge application requiring escalation. CLD-0235 involved a successful MFA approval after repeated denied prompts, requiring investigation of the account and active session. CLD-0236 confirmed LSASS memory access before EDR terminated the process, with no verified authorization for the claimed security testing. The next shift should follow up on escalations, verify containment and remediation, and monitor for additional suspicious activity.

## Cloudora · Shift 10 · 2026-10-19

Completed investigations for CLD-0237 through CLD-0240, with all four alerts closed in the queue. CLD-0237 and CLD-0240 identified suspected vendor impersonation and payment-redirection activity involving a potential £84,200 payment, including an earlier suspicious email delivered during the CLD-0220 subscription flood. CLD-0238 involved an elevated payroll run associated with documented change CHG-2112, while CLD-0239 involved DMARC failures largely attributed to an unconfigured marketing mail provider, with remaining sources requiring review. The next shift should verify that no fraudulent payment or banking-detail change occurred, confirm appropriate containment of suspicious emails, and follow up on outstanding email authentication findings.

## Cloudora · Shift 11 · 2026-10-20

Closed all four incidents for this shift. CLD-0241 identified historical operator activity, but log retention limits prevented confirming earlier compromise. CLD-0242 confirmed an unauthorized anonymous sharing link that was later revoked. CLD-0243 identified a departing employee syncing 11 GB of company files to an unmanaged device and requires further investigation. CLD-0244 involved a request to reactivate a suspended guest account without completed security clearance. The next shift should follow up on the data exposure investigation, verify remaining sharing links, and ensure the guest account stays suspended until approved.

## Cloudora · Shift 12 · 2026-10-21

Completed investigations for CLD-0245 through CLD-0248. CLD-0245 was escalated due to Sam Okoro accessing sensitive repositories outside his normal pattern, while CLD-0246 was identified as an authorized platform handover download. CLD-0247 confirmed a password-spraying attack against 214 accounts, with no successful authentication identified. CLD-0248 confirmed an attempted USB transfer where 40 files (180 MB) were written before DLP blocked further copying. All four tickets are closed, but the next shift should follow up with Security, HR, and Legal regarding Sam Okoro's activity, investigate the transferred files, and continue monitoring for suspicious sign-ins.

## Cloudora · Shift 13 · 2026-10-22

Completed investigations for CLD-0249 through CLD-0252. CLD-0249 identified an anonymously accessible payroll file containing sensitive employee information, requiring privacy and security escalation. CLD-0250 identified an unauthorized inbound mail connector bypassing spam and phishing protections, while CLD-0251 identified an MFA policy exclusion requiring review. CLD-0252 confirmed a successful legacy IMAP4 login without MFA from a source range associated with password spraying. All four tickets are closed in the queue, but the next shift should follow up on containment, configuration changes, account security, and outstanding escalations.

## Cloudora · Shift 14 · 2026-10-27

Completed investigations for CLD-0253 through CLD-0256, with all four tickets closed in the queue. CLD-0253 confirmed an Excel attachment triggered encoded PowerShell and downloaded a suspicious payload on LDN-WS-141, while CLD-0255 confirmed antivirus and tamper protection were disabled on the same workstation approximately 90 minutes later. CLD-0254 was classified as a false positive because the encoded PowerShell originated from a documented nightly backup task. CLD-0256 confirmed a malicious macro-enabled attachment from a compromised supplier account reached nine finance recipients, with two opening it. The next shift should follow up on endpoint containment, investigate both recipients who opened the attachment, verify mailbox remediation, and confirm security protections have been restored.

## Cloudora · Shift 15 · 2026-10-28

Completed and closed all four incidents: CLD-0257, CLD-0258, CLD-0259, and CLD-0260. CLD-0257 documented three detection improvement proposals for October security incidents. CLD-0258 identified excessive false-positive alerts from scheduled payroll activity, while CLD-0259 identified a potential mailbox export detection gap requiring rule validation. CLD-0260 involved suspicious external sharing links to a personal email address and was recommended for escalation. No tickets remain open in the shift queue; the next shift should follow up on detection-rule tuning, mailbox export coverage, and potential unauthorized access through the external sharing links.

## Cloudora · Shift 16 · 2026-10-29

Completed and closed all four incidents: CLD-0261, CLD-0262, CLD-0263, and CLD-0264. CLD-0261 involved a suspected payroll phishing campaign with one observed credential submission; recipient verification and containment require follow-up. CLD-0262 involved an unsuccessful executive impersonation attempt to reset MFA, which the helpdesk prevented through proper verification procedures. CLD-0263 was determined to be a false positive involving an approved OAuth application, while CLD-0264 identified a guest MFA policy enforcement gap requiring remediation. No incidents remain open in the shift queue; the next shift should verify phishing containment, review executive account security, and confirm that guest MFA enforcement has been corrected.

## Cloudora · Shift 17 · 2026-11-02

Completed investigations for CLD-0265 through CLD-0268. CLD-0265 and CLD-0266 were classified as false positives based on legitimate employee onboarding activity and approved remote work in Portugal. CLD-0267 was identified as suspected data exfiltration involving a 340 MB encrypted archive uploaded to personal cloud storage after access to 412 HR personnel files; urgent investigation and containment are recommended. CLD-0268 involved a confirmed third-party authentication database breach at ExpenseFlow, potentially exposing credentials belonging to 150 employees. The next shift should prioritize verifying the contents and exposure of the encrypted archive, coordinating ExpenseFlow password resets and vendor remediation, and monitoring for suspicious authentication activity. Both high-severity investigations require follow-up until containment and remediation are verified.

## Cloudora · Shift 18 · 2026-11-03

Completed Shift 18 investigations for CLD-0269 through CLD-0272. All four tickets were closed in ServiceNow, with unresolved security concerns documented for follow-up. CLD-0269 involved an unverified device registration, while CLD-0270 identified a mailbox rule copying sensitive business emails to an internal distribution list requiring recipient verification. CLD-0271 involved unusually high printing activity from the Customer-Contracts library, and CLD-0272 identified a legacy VPN session operating without MFA enforcement. The next shift should prioritize verifying Priya Nair's device authorization, reviewing distribution list membership, investigating the bulk printing activity, and remediating the VPN MFA gap. These related events should be correlated to determine whether they indicate broader account compromise.

## Cloudora · Shift 19 · 2026-11-04

Completed Shift 19 investigations for CLD-0273 through CLD-0276, with all four tickets closed in ServiceNow. Peer reviews identified insufficient technical justification in a phishing investigation, an unnecessary impossible-travel escalation, and an incorrectly closed MFA denial alert involving privileged account svc-deploy. CLD-0276 identified a scheduled PowerShell task on LDN-SRV-CI1 with discrepancies from approved change CHG-2131. No tickets remain open in the queue, but the next shift should prioritize svc-deploy credential rotation, verification of the scheduled task and script integrity, and follow-up on the identified analyst QA deficiencies.

## Cloudora · Shift 20 · 2026-11-05

Completed Shift 20 investigations for CLD-0277 through CLD-0280, with all four tickets closed in ServiceNow. Reviewed the October security engagement report, including incidents, control improvements, and outstanding risks. Key unresolved issues include ExpenseFlow credential reuse exposure, incomplete offboarding for sam.okoro@cloudora.io, and the guest MFA policy gap affecting kmarsh.ext@cloudora.io. The next shift should verify credential reset completion, revoke remaining sharing links and repository tokens, confirm containment of the active guest session, investigate related activity, and ensure guest MFA enforcement is corrected.

## Larkspur Home · Shift 21 · 2026-11-06

Completed investigation of all four alerts during Shift 1.

LRK-0301 involved AWS root account activity and was reviewed against administrative support procedures. LRK-0302 involved an MFA reset and new device sign-in, which was supported by helpdesk ticket HD-6011. LRK-0303 involved SQL injection attempts against the /search endpoint, with 1,240 malicious requests blocked by AWS WAF. LRK-0304 involved publicly exposed SSH access on staging-bastion, where GuardDuty detected 63 probes from 19 IP addresses.

All four incidents are marked closed in the training queue. No incidents remain open. The next shift should monitor for additional SQL injection attempts, verify that the temporary SSH security group rule has been removed, and watch for unauthorized access attempts or suspicious authentication activity.

## Larkspur Home · Shift 22 · 2026-11-10

Completed all four investigations (LRK-0305 through LRK-0308), with no tickets remaining open in the queue. LRK-0305 involved unauthorized payment-page script tampering and was escalated for incident response; LRK-0306 involved a suspicious delivery email; LRK-0307 involved an impossible-travel alert requiring VPN verification; and LRK-0308 confirmed an overly permissive S3 bucket policy exposing customer information. The next shift should monitor payment-page remediation and customer impact, verify that S3 public access has been restricted, and follow up on any outstanding incident response actions. All investigation findings and recommended actions have been documented.

## Larkspur Home · Shift 23 · 2026-11-11

Completed investigation and closed all four alerts (LRK-0309 through LRK-0312). LRK-0309 involved compromised Brightwave IAM credentials and unauthorized AWS API activity; credentials were deactivated and remediation remains in progress under SEC-0412/SEC-0413. LRK-0310 involved repeated AWS console logins without MFA using a shared service account password; the access pattern was consistent with historical activity, but the credential-sharing risk remains unresolved under HD-5980. LRK-0311 was confirmed malware successfully quarantined before execution, with a clean follow-up scan. LRK-0312 was an approved temporary Okta Super Administrator assignment, subsequently revoked as scheduled. No SOC alerts remain open; the next shift should monitor outstanding credential remediation and unauthorized activity involving Brightwave, and follow up on the shared service account access risk.

## Larkspur Home · Shift 24 · 2026-11-16

Completed investigation and closed all four alerts (LRK-0313 through LRK-0316). LRK-0313 involved unauthorized payment-page script modification, with the compromised key disabled and the clean script restored. LRK-0314 involved an unexpected MFA push requiring continued monitoring of suspicious authentication activity. LRK-0315 confirmed attempted audit logging tampering, but AWS denied both requests. LRK-0316 identified production API load testing outside the approved staging scope, with WAF rate limits successfully blocking excessive traffic. No alerts remain open in the queue; the next shift should monitor the ongoing payment-page incident, suspicious authentication activity, and any further unauthorized production testing.

## Larkspur Home · Shift 25 · 2026-11-17

Completed investigations for LRK-0317, LRK-0318, LRK-0319, and LRK-0320; all four tickets are closed. LRK-0317 and LRK-0318 involved payment-page security concerns, including CSP violations and cached script delivery after invalidation. LRK-0319 involved a Portugal sign-in supported by a documented travel notice and registered device. LRK-0320 involved an approved GPU instance associated with elevated AWS spending, but its shutdown status and actual cost impact remain unverified. The next shift should monitor payment-page integrity, confirm the GPU instance is stopped, and review AWS billing for any continued unexpected spending.

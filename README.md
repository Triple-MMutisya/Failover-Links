# Failover-Links
Configuring Failover using Recursive Routes
🚀 𝐌𝐚𝐬𝐭𝐞𝐫𝐢𝐧𝐠 𝐈𝐒𝐏 𝐅𝐚𝐢𝐥𝐨𝐯𝐞𝐫 𝐨𝐧 𝐌𝐢𝐤𝐫𝐨𝐓𝐢𝐤 𝐰𝐢𝐭𝐡 𝐑𝐞𝐜𝐮𝐫𝐬𝐢𝐯𝐞 𝐑𝐨𝐮𝐭𝐞𝐬 & 𝐄𝐦𝐚𝐢𝐥 𝐌𝐨𝐧𝐢𝐭𝐨𝐫𝐢𝐧𝐠 🚀

In modern networks, uptime is everything. To ensure continuous connectivity, I recently configured a dual ISP failover on MikroTik using recursive routing.

🔹 𝐖𝐡𝐲 𝐑𝐞𝐜𝐮𝐫𝐬𝐢𝐯𝐞 𝐑𝐨𝐮𝐭𝐞𝐬?
Unlike simple distance-based failover, recursive routes allow the router to 𝐜𝐡𝐞𝐜𝐤 𝐢𝐟 𝐚 𝐫𝐞𝐚𝐥, reachable IP (like Google DNS 8.8.8.8) is available through the gateway.

I𝐟 𝐭𝐡𝐞 𝐈𝐏 𝐢𝐬 𝐧𝐨𝐭 𝐫𝐞𝐚𝐜𝐡𝐚𝐛𝐥𝐞 → the route is withdrawn.
𝐈𝐟 𝐫𝐞𝐚𝐜𝐡𝐚𝐛𝐥𝐞 → traffic flows normally.

This ensures the router doesn’t just see a “link up” status but actually verifies end-to-end internet reachability.

🔹 𝐌𝐲 𝐒𝐞𝐭𝐮𝐩:
Primary ISP → 𝟏𝟎.𝟏𝟎.𝟏𝟎.𝟐/𝟐𝟗
Secondary ISP → 𝟏𝟎.𝟓𝟎.𝟓𝟎.𝟐/𝟐𝟗
Recursive Route Check → 𝟖.𝟖.𝟖.𝟖 & 𝟏.𝟏.𝟏.𝟏

🔹 𝐀𝐮𝐭𝐨𝐦𝐚𝐭𝐢𝐨𝐧 𝐰𝐢𝐭𝐡 𝐌𝐨𝐧𝐢𝐭𝐨𝐫𝐢𝐧𝐠:
I integrated 𝐍𝐞𝐭𝐰𝐚𝐭𝐜𝐡 + 𝐄𝐦𝐚𝐢𝐥 alerts so the router automatically notifies me when:
✅ Primary ISP goes DOWN (failover activated)
✅ Primary ISP comes BACK UP (restored as preferred route)

📧 𝐄𝐱𝐚𝐦𝐩𝐥𝐞 𝐚𝐥𝐞𝐫𝐭:
“⚠️ Primary ISP is DOWN. Traffic routed via Backup ISP.”

💡 𝐊𝐞𝐲 𝐓𝐚𝐤𝐞𝐚𝐰𝐚𝐲:
By combining recursive routing with email notifications, network admins can:
✔ Achieve seamless ISP failover
✔ Detect real internet outages (not just link down events)
✔ Stay informed in real-time for proactive troubleshooting

🔧 𝐍𝐞𝐱𝐭 𝐒𝐭𝐞𝐩: I’m expanding this setup to include load balancing + SMS alerts for even more resilience.

#MikroTik #Networking #Failover #Automation #NetworkEngineering #Resilience

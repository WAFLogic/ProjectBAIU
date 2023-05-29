# ProjectBAIU
The most powerful, extensible, customizable, TRUE DDoS, and TRUE Distributed Brute Force Prevention tool since 2012 (compare it, I dare you :D ) and now it handles all ports and protocols, not just HTTP/S!

BAIU is a (royalty free) patent pending, world first rate limiter that has saved Choice Hotels half a million dollars in digital theft in one year already, reducing the losses from over $8,000 weekly to $0 i.e. 100% resolution and with proper configuration thus far has been able to boast 99.9999% accuracy while handling over 60,000 unique events daily.

What is Project BAIU?
It's the B(ad) A(ss) I(P) U(ser) Rate Limiter!

BAIU will actively monitor, and/or restrict the ability of network based entities, both human and automated software, accessing certain aspects of a hosted site that is viewable on the internet over periods of hours, to days, to weeks, to months with multiple, user-defined, variable control methods for restriction, event triggers, multiple methods of counting IP and/or UserID access, and multiple variable, user-defined timing controls that set independent timing constraints for monitoring and restricting IP/UserID access. It is capable of monitoring and restricting via a static and dynamically distributed model when monitoring and restricting IPs and/or userID/strings. Monitoring and restricting over customizable periods of time (hours, days, weeks, months) significantly reduces the daily chances of attacks. Rather than the "here and now" approach commonly used, BAIU registers, catalogs, analyzes, trends, and considers behavioral characteristics to determine the appropriate reaction. This is the core of the static monitoring and restriction functionality. At this time BAIU only works for the F5 networking appliances as long as the F5 can process iRules which is every appliance they made regardless of licensing. A10 has developed a load balancer/WAF combo that support iRules through conversion and this code is all TCL based so theoretically it can be ported to virtually any system that supports TCL and a database.

The primary focus is for brute force events on login pages however the rate limiter can be used for any URI desired. It just depends on how basic to advanced you want it! You can simply rate limit by IP counting over hours, days, to weeks, or do the same and extend it to use userIDs or any input string for that matter using several methods of correlation which include bad password detection, UserID guessing, UserID brute force list with single to many IPs, etc. This is the most robust and versatile rate limiter that exists in this world today, for the time being. And it's free to use!

Currently this only works on F5 systems but it will work on anything they have so long as it supports iRules. A10 is also a vendor that support iRule conversion to run on their system so this already has potential portability. The code is all TCL so theoretically it can be ported anywhere that supports TCL and a database to track data.

So there's a lot to the code that you can find on the download page. Check it out and have fun with it! We do provide consultation services to explain how this works and can even help you set it up for your organization. Just contact us and we'll help you out.

I intend for this site to also be a portal to share events and attacking IP sources to help the world as a whole track down and prevent these highly diverse & organized hackers.

I also intend for this site to provide the BAIU code for other platforms as it becomes available. As time and the community makes this happen, it will become available. A10 load balancers that support iRules will likely be the first to test on work on porting this over to other platforms.

So that's the intro. Below is the information submitted for the patent paperwork which describes BAIU much more in-depth including it's features, what it really does for us, and why you probably need it for your web site especially if you have anything digitally sensitive that is accessible via the internet.

(a) Problem To Be Solved By The Invention / Purpose Of The Invention:
The problem being solved is the inability of web sites to differentiate criminals from legitimate users. The specific example that led to this invention is the use case of criminals taking advantage of the inability to discern legitimate from malicious users and hacking into user accounts, gaining access to sensitive user data, and stealing credits or points that can, through various methods, be converted to money.

Criminals are using a highly diverse set of computers in their attacks. These computers are likely normal computers that have been compromised with malicious software. This malicious software, also known as â€œmalwareâ€, is often running unknown to the owner of the computer.

The criminals also have lists of hacked user names and passwords that people have set up for various website accounts, such as social networking and travel sites. This gives the criminals a vast, varied, and seemingly legitimate set of computers on the internet, and also lists of usernames and passwords to one or more websites. With this, the criminals then launch attacks from this network of computers, against various websites, using those or similar usernames and passwords. Since many people use the same or similar usernames and passwords across multiple accounts, the criminals are often able to get access to user accounts on these various websites.

Identifying and blocking these criminals remains a current security challenge for companies that provide web content and have something of value that is protected by means of user authentication. This invention can potentially be used by anyone running a website that needs to differentiate between legitimate and malicious users.

(b) How the problem is currently solved:
Currently, Transaction Rate Limiters (TRLs) and TRUE Distributed Brute Force Prevention Utilities (BFUs) have limited user recognition functionality which relies on correlating and identifying traffic trends based on IP address and, in some cases, a userID/string element, for a static, per moment, event; â€œhere and nowâ€. The TRLs and BFUs monitor events in transactions per second, per minute, and/or per hour. The attacking group(s) are skilled enough to work around this limited functionality and have an attack footprint that utilizes thousands of source IP addresses and span time periods of hours, days, and weeks.

Example:

3,000 IPs with a single TRL with a limit of 10 transactions per second allows for 2,592,000,000 chances for a successful attack.

(c) How Invention Solves The Problem:
The BAIU (Basic to Advanced IP & UserID) Rate Limiter is designed to actively monitor, and/or restrict the ability of network based entities, both human and automated software, accessing certain aspects of a hosted site that is viewable on the internet over periods of hours, to days, to weeks, to months with multiple, user-defined, variable control methods for restriction, event triggers, multiple methods of counting IP and/or UserID access, and multiple variable, user-defined timing controls that set independent timing constraints for monitoring and restricting IP/UserID access. It is capable of monitoring and restricting via a static and dynamically distributed model when monitoring and restricting IPs and/or userID/strings.

Monitoring and restricting over customizable periods of time (hours, days, weeks, months) significantly reduces the daily chances of attacks. Rather than the â€œhere and nowâ€ approach commonly used, BAIU registers, catalogs, analyzes, trends, and consider behavioral characteristics to determine the appropriate reaction. This is the core of the static monitoring and restriction functionality.

Begin Section C Reference (1):
With the example defined in response (B) and BAIU configured with a limit of 12 userIDs per IP, and 6 IPs per userID, 40 requests per IP, 30 requests per userID, and one instance of BAIU we now have a maximum daily chance at attacking 36,000 unique accounts, with a maximum possibility of chances of successful attack being 120,000.

This is over a 99.99% reduction of chances from a non-BAIU protected system. These are the highest mark numbers possible, however due to the behavioral characteristics BAIU is capable of correlating, the number of chances are significantly reduced even further. The key concept to BAIU is the harder an attacker typically works to compromise the website, the better and faster BAIU works against them.

For example, if 1 userID is called by 4 different IPs one time, all 4 IPs and the userID are now blocked. This eliminates 5 threat vectors reducing the maximum chances of unique userIDs by 66 in 5 requests. Depending on configuration, this also now means all subsequent IPs trying the blocked userID could now be blocked. If 12 IPs call the blocked UID, the maximum chances of unique userIDs attempts are now reduced 144.

When adding theory of probability the maximum chances are even further reduced when using the behavioral/anomaly capabilities of BAIU raising the possibility to reduce threats to a theoretical 100% over time which is un-claimable by any other system.

In most attack scenarios, whether distributed, dynamic and distributed, or just brute force, BAIU handles the scenarios effectively and according to configuration with exceptional accuracy and results.

Currently with 23,000~ IPs and about 36,000~ unique userIDs monitored daily, BAIU (two instances across two F5 3900 appliances actively syncing their ban/request list every 5 minutes and 59th minute of the hour) actively ban roughly 80~ unique IP and about 70~ unique userIDs daily for all production Choice Hotels International, Inc.â€™s consumer web sites.

End Section C Reference (1).
(d) Specific Features that Make this Invention Novel:
UserID/string simplification to ensure tracking of only useful IDs/strings, and ensure variances of the same element is tracked as one rather than uniquely.

Traditional TRLs and BFUs have a static approach when tracking a userID/string element to monitor. To support accurate anomaly detection, BAIU uses a simplification process when monitoring a string to ensure almost any combination of a string value that would still be associated with a single account element, will be handled as a single element rather than multiple variations that could be handled uniquely.

String manipulation/simplification functionality is all Configuring User/Organization (CU/O) defined. The inventorâ€™s standard approach would be to set all characters to lower case, remove the @ character and all trailing string elements leaving only the user ID portion, then remove all special characters and punctuation, setting all digits to 0 or like character, finally having a simplified ID to now track. This is just one approach, and other concepts or variances of this setup can be used.

The simplification process is to ensure a single user who has mistyped their userID/string element or is trying multiple variations of what would likely be perceived as the same userID/string element remains as a single element. It also negates chances of tracking userIDs/strings that do not conform to a site's userID/string standard such as too long, too short, and even de-obfuscating code based attack strings such as a SQL Injection attack. This ensures the least, but most effective elements, are tracked and available for monitoring and/or restriction. The manipulation is only done for the monitoring and restricting device as well so that the tracking string is not manipulated at the TCP/UDP packet level, only in device memory.

An example of userID simplification would be as follows: â€œBilbo.Hoppins@example.comâ€, â€œBilbo_hoppins@example.comâ€, â€œBiLBo_._HoPPiNSâ€, â€œB.I#.!lB(O)+=HoP!$,.P?i/nSâ€, will all be tracked as â€œbilbohoppinsâ€. This is part of the dynamic monitoring and restriction functionality.

Track/correlate multiple IPs querying a single userID/string, and track/correlate a single IP querying multiple UserIDs/strings. This ensures events that are relevant/similar through correlation, will be handled as one, accordingly (Many to One).

Traditional TRLs and BFUs typically consider events either per IP, or per userID/string. BAIU monitors and restricts the limit of userID/strings called by a single IP. It also monitors and restricts the number of IPs that have called a userID/string. This ensures a dynamically distributed chain of events for an IP/userID/string is more likely to be treated as a singular set of entities and events, rather than separate entities and events. A potential standard would be a limit of 15 userIDs per IP, and 6 IPs per userID. Anything equal to, or more, would invoke a restriction event. This is the core of the distributed dynamic monitoring and restriction functionality.

IP Geo-location service inclusion for IP locality correlation (Many to One).
BAIU is capable of utilizing IP Geo-location logic in the Many to One correlation described above. For example, BAIU can perform zip code analysis and, if zip codes differ by a defined amount, invoke a monitoring or restricting event.

Basic to advanced defined logic to detect static or dynamically distributed events that can be configured by a CU/O to meet the specific trends and criteria that would deem traffic questionable/malicious/undesired.

Event triggers are defined uniquely and as extensively as the CU/O chooses. Event triggers could be any defined HTTP/TCP/UDP based event(s) that would be deemed as malicious/negative/undesired by the CU/O. Examples could be an HTTP response code, or the existence/non-existence of a cookie. Malicious/negative/undesired events will cause the request counter for the identified IP/userID/string element to increase by 1 and by the amount set in the multiplier value. The purpose is to have valid sessions have a standard request rate of 1, while other events that meet a malicious/negative/undesired eventâ€™s criteria have a standard request rate of greater than 1. This ensures malicious/negative/undesired elements reach a given threshold much faster than normal. This is part of the dynamic monitoring and restriction functionality.

Customizable time-periods for monitoring and restricting based on IP/UserID/String and their restricting or monitoring events.
Restrictions are fully definable for IP and userID/string values with features that can be enabled and disabled during run time. The standard approach is for IPs and userID/strings to have independent timing values that can be chosen from three timing value sets; Standard, Half, and Long. Each timing value set has timing values for banning and monitoring. More or less timing values can be used depending on need of complexity.

The standard approach to restriction configuration is to restrict for a Standard ban time and add the given element to the Long period of time tracking. Upon release of restriction, if the element continues to hit the thresholds configured to invoke restriction within the Long period of monitoring, then the Long ban value will be used and the Long timer will be reset. Single occurrence offenders are released in a standard time, while repeat offenders will be restricted for the Long time period.

Specific triggers to increase counters more rapidly to ensure an element is moved to a restricting event sooner upon CU/O defined criteria that is deemed malicious.
A multiplier is used for event triggers to define the value that a request should be incremented by to effectively increase the request counts faster for the actual request. Event action has a CU/O setting to trigger quicker action. This is the core to the anomaly detection.

Configurable monitoring and restriction thresholds.
Restriction and event actions can be initiated based on configured thresholds per IP and UserID/string. Thresholds are also considered when setting multiplier values.

Specific events for post-restricting activity, such as resetting counters for repeat traffic during restriction.
A further expansion on restriction capabilities is the ability to generate a new action upon events that occur during the restriction time frame. For example, restriction time can be based on the most recent event ensuring a "rolling" restriction occurs and the element is never dropped from restriction until that element no longer generates events during the configured time period. Additionally, there is an ability to restrict all IP/userID/string elements that call an element that has already been restricted. Other events besides a restriction event can be defined instead, with restriction being the standard action.
Manual interaction/manipulation of monitored and restricted elements by the CU/O.
A set of Administration URIs that are custom defined by the CU/O allow administration of the monitoring and restriction settings for IP/userID/string elements. These URIs give specific control to add, remove, and edit entries that are actively being monitored and restricted. This gives granular manual control to the CU/O beyond the automated capabilities.

The primary function of the Administration URIâ€™s is to add and remove elements from the monitoring and restriction tables. However, CU/O can define capabilities such as setting request counts to maximum to ensure given element makes more interaction with the BAIU rate limiter which allows other counters the chance to increase if said elements invoke any events.

An example would be to max an IPâ€™s request count so that when it makes another connection, the userID element is also considered for monitoring and/or restriction.

Synchronization of monitoring and restricting events across multiple platforms that the mechanism has been built/cloned on to create distributed load while ensuring events are tracked equally.

The Administration URIs can be directly accessed within the siteâ€™s defined control parameters and called via each device (BAIU capable or not) at a manual or timed interval through such means as a cronjob. The devices(s) parse through all logged restriction events within a CU/O defined interval, and at a said interval defined by the CU/O, will call all other BAIU functional devices via the Administrative URI for that function to add/drop all restricted/dropped IP/userID/string elements. This effectively allows synchronization of all restricted/dropped elements across all devices that have BAIU enabled.

Real-time monitoring of all events can be configured as well to ensure real-time synchronization using the same methods or a combination there-of could be used depending on the CU/Oâ€™s needs.

+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Use Case Information:
Comparative analysis does not exist for the capabilities and elements available for monitoring over the length of times specified. So far an F5 3900 appliance (Specifications available at www.f5.com/pdf/products/big-ip-platforms-datasheet.pdf) has been used and it has been proven successfully capable of tracking 116,280 unique elements over 7 days, and 8 hours successfully, accurately, at an atomic clock level (thanks to F5 appliance) without any increase in standard CPU or RAM/memory usage upon memory usage/consumption that occurs normally by design via the Linux core kernel memory usage standards. The appliances have never broken 68.2% memory usage with an average reserve load of 66.6% which is standard with/out BAIU being loaded i.e. standard production usage.
2.8k~ connections per second have been successfully loaded through BAIU over a week time period on several test scenarios with no performance impact experienced as well with the F5 3900 appliance.

The appliances running BAIU remain fully functional without any issue after 4+ months running.

Please refer to Section C Reference (1) for additional commentary.
(e) Other Inventions That Address The Same Problem:
F5 ASM provides â€œBrute Force Preventionâ€ functionality in an attempt to address the same problem as this invention. There are also other various rate limiters and brute force remediation tools that offer limited analysis, correlation, and response functionality.

(f) Shortcomings/Disadvantages Of Other Inventions:
Other products, such as the F5 ASM, do not offer all of the malicious traffic identification logic, the static and dynamic control methods, the userID simplification functionality, or the granular configuration and user control options and flexibility.

When configuring this feature with a similar set of thresholds as defined in Section C Reference (1), it was incapable of restricting a single event BAIU restricted in production traffic due to the method of throttling used by the attacking parties.

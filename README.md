# ClassicUO-Angel-Island-Version
Optional Client for Angel Island. Modified to ensure players are not creating/using more accounts on Angel Island than allowed.

# What does it do and how does it work

1. We define new packets to support a mild cryptographic handshake with ClassicUO.</br>
If CUO fails the handshake, and ForceGMNCUO is set, the user will get a dialog about 20 seconds after logging in informing them of the rule, and that they will be disconnected or warned.
This feature is optional and can be turned on/off server-side.</br>
2. We send the standard OSI 0xD9 packet to the server. This packet is basically a collection of 'machine info'. The server uses a hash of this machine info to identify players trying to connect more than one account to our server (even if they are using a different IP Address.)</br>
See Scripts\Misc\HardwareInfo.cs in the server for a complete explanation.

# Powercord Community Guidelines
These guidelines are set to ensure Powercord's ecosystem stays as awesome as possible, and to avoid malicious plugins,
or plugins performing badly. The Powercord Staff will enforce **all** of these guidelines and take decisions we consider
appropriate for plugins not complying with these guidelines, at our sole discretion.

**Note**: We may decide, depending on the context, to let uncompliant plugins pass. These exceptions will be made at our sole discretion.

## Definitions
 - Product: Either a plugin or a theme for Powercord
 - Discord API: All remote services hosted by Discord (REST API, Gateway, CDN, Media Proxy, ...)
 - End User Data: Any data (username, avatar, messages, ...) posted or otherwise generated by Discord users
 - Selfbotting: The automation of any action interacting with the Discord API with a disproportionate amount of manual user interaction. Note that a single user interaction should only trigger one (or depending on the context, a small amount) interaction with the Discord API. You may not perform bulk operations to the Discord API based on a single user input. You also may not perform actions normally impossible for a normal client, such as sending embeds.

## The rules
Everything you build for Powercord will have to follow those rules.

### 1. Do not promote or facilitate abusive behavior
This includes but is not limited to:<br>
  - Any behavior that breaks Discord's ToS (excluding client modding);<br>
  - Any behavior that would abuse the Discord API;<br>
  - Distributing malicious and/or harmful plugins (malware);<br>
  - Distributing plugins which serve to confuse and/or annoy users.<br>
    - For example: spoiler-spam, exploit of obscure client behavior.

### 2. Take precaution handling End User Data
End User Data of other users must be handled with caution with regards to privacy. For example, logging all deleted messages is prohibited.

### 3. Do not attempt to circumvent Discord permissions
Any data processed from Discord API endpoints must be processed the same way as it is by the Discord client UI.<br>
For example, displaying channels that the Discord client would otherwise hide is prohibited.<br>
This also applies to restrictions put in place by Discord on legal or any other serious matters, such as the NSFW age gate.

### 4. Plugins are prohibited from implementing selfbot-like behavior
This is to ensure our users do not get banned from indirect ToS violations, and to avoid abuse.

### 5. No advertising, promotion, or spam of any kind
Your plugin is prohibited from advertising anything on the Discord client.<br>
Powercord provides links to your GitHub account, product repository, and a link to your product's Discord support server if provided.<br>
Degrading the user experience through unnecessary messages or pop-ups shown in-app also falls under this rule.

### 6. Respect user privacy
If your plugin has a backend, this backend is prohibited from storing any user data without explicit permission from the plugin user.<br>
All features that require the collection of user data should be opt-in, and properly reflect data collection via the `use_eud` permission.

### 7. Take precaution making use of external APIs
The use of external APIs may put the user's privacy at risk.<br>
Remote services may keep track of user IPs and more.<br>
If your plugin makes use of a remote service, please specify this with the `ext_api` permission.

Fetching arbitrary URLs (e.g. pinging of links posted in chat) must go through a proxy server.

### 8. Take precaution creating NSFW plugins
We're not against plugins providing NSFW features, but they should be properly labeled and handled.<br>
If your plugin's main purpose is providing NSFW content, you must specify this through the `nsfw` manifest key.<br>
If your plugin's main purpose isn't necessarily providing NSFW content, but your plugin can provide NSFW content, the NSFW features must be disabled by default.

### 9. Meet a certain standard performance-wise
Products that demand a lot of resources degrade the user experience. Slower computers may not be able to run smoothly if your product is using excessive amounts of CPU and/or memory.

If you do need to perform resource-heavy tasks, consider using a [web worker](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers).

### 10. Avoid breaking other plugins
In the event your plugin breaks with another plugin, we expect you and the other developer to get in touch and figure out a solution to the problem. It's all about friendly cooperation.

### 11. Prefer contributing instead of duplicating
If you want to make a plugin that already exists, prefer contributing to the already existing plugin instead of having another plugin with the same purpose.

## How we handle plugins
### Size doesn't matter
This is also true for plugins. Your plugin can be very feature rich with thousands of lines of code, or just a few
lines. As long as they bring a feature, we'll accept it.

To quote aetheryx,
> plugins are like boobs<br>
> small, big, it doesn't matter, we love them all

### We'll always let people decide how they write their code
When reviewing plugins, we won't impose any specific code style, license or anything. Your code, your choices. We'll
recommend some good practices (like not mixing `"` and `'` for example), but won't reject your plugin because of it.

### We will never directly push to your plugin's repo
Even if we have full access by being administrators of the organization, we'll never push to a plugin's repo unless
we're invited to do so. We'll always prefer forking and making a PR. It's your plugin, and we don't have to push. The only exception to this is an urgent security vulnerability; in the case of a high-risk vulnerability, we may hotfix your plugin to prevent widespread damage to users.

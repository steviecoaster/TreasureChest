---
external help file: NexuShell-help.xml
Module Name: NexuShell
online version:
schema: 2.0.0
---

# New-NexusDockerProxyRepository

## SYNOPSIS

Creates a new Conda Proxy Repository

## SYNTAX

### Default (Default)

```powershell
New-NexusDockerProxyRepository -Name <String> [-Online] [-BlobStoreName <String>] [-UseStrictContentValidation]
 [-CleanupPolicy <String>] -ProxyRemoteUrl <String> [-ContentMaxAgeMinutes <String>]
 [-MetadataMaxAgeMinutes <String>] [-UseNegativeCache] [-NegativeCacheTTLMinutes <String>]
 [-RoutingRule <String>] [-UseNexusTrustStore] [-BlockOutboundConnections] [-EnableAutoBlocking]
 [-ConnectionRetries <String>] [-ConnectionTimeoutSeconds <String>] [-EnableCircularRedirects] [-EnableCookies]
 [-CustomUserAgent <String>] [-EnableV1] [-ForceBasicAuth] [-HttpPort <String>] [-HttpsPort <String>]
 [-ProxyIndexType <String>] [-IndexUrl <String>] [<CommonParameters>]
```

### Authentication

```powershell
New-NexusDockerProxyRepository -Name <String> [-Online] [-BlobStoreName <String>] [-UseStrictContentValidation]
 [-CleanupPolicy <String>] -ProxyRemoteUrl <String> [-ContentMaxAgeMinutes <String>]
 [-MetadataMaxAgeMinutes <String>] [-UseNegativeCache] [-NegativeCacheTTLMinutes <String>]
 [-RoutingRule <String>] [-UseNexusTrustStore] [-UseAuthentication] -AuthenticationType <String>
 -Credential <PSCredential> [-HostnameFqdn <String>] [-DomainName <String>] [-BlockOutboundConnections]
 [-EnableAutoBlocking] [-ConnectionRetries <String>] [-ConnectionTimeoutSeconds <String>]
 [-EnableCircularRedirects] [-EnableCookies] [-CustomUserAgent <String>] [-EnableV1] [-ForceBasicAuth]
 [-HttpPort <String>] [-HttpsPort <String>] [-ProxyIndexType <String>] [-IndexUrl <String>]
 [<CommonParameters>]
```

## DESCRIPTION

Creates a new Conda Proxy Repository

## EXAMPLES

### EXAMPLE 1

```powershell
New-NexusDockerProxyRepository -Name DockerProxyTest -ProxyRemoteUrl https://hub.docker.io -Online
```

## PARAMETERS

### -Name

The name to give the repository

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Online

Mark the repository as Online.
Defaults to True

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobStoreName

The back-end blob store in which to store cached packages

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseStrictContentValidation

Validate that all content uploaded to this repository is of a MIME type appropriate for the repository format

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -CleanupPolicy

The Cleanup Policy to apply to this repository

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProxyRemoteUrl

Location of the remote repository being proxied, e.g.
https://api.Conda.org/v3/index.json

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentMaxAgeMinutes

Time before cached content is refreshed.
Defaults to 1440

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1440
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetadataMaxAgeMinutes

Time before cached metadata is refreshed.
Defaults to 1440

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1440
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseNegativeCache

Use the built-in Negative Cache feature

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -NegativeCacheTTLMinutes

The Negative Cache Time To Live value.
Defaults to 1440

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1440
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoutingRule

Routing Rules you wish to apply to this repository

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseNexusTrustStore

Use certificates stored in the Nexus truststore to connect to external systems

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseAuthentication

Use authentication for the upstream repository

```yaml
Type: SwitchParameter
Parameter Sets: Authentication
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationType

The type of authentication required by the upstream repository

```yaml
Type: String
Parameter Sets: Authentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential

Credentials to use to connect to upstream repository

```yaml
Type: PSCredential
Parameter Sets: Authentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostnameFqdn

If using NTLM authentication, the Hostname of the NTLM host to query

```yaml
Type: String
Parameter Sets: Authentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainName

The domain name of the NTLM host

```yaml
Type: String
Parameter Sets: Authentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockOutboundConnections

Block outbound connections on the repository

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoBlocking

Auto-block outbound connections on the repository if remote peer is detected as unreachable/unresponsive

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionRetries

Connection attempts to upstream repository before a failure

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionTimeoutSeconds

Amount of time to wait before retrying the connection to the upstream repository

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableCircularRedirects

Enable redirects to the same location (may be required by some servers)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableCookies

Allow cookies to be stored and used

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomUserAgent

Custom fragment to append to "User-Agent" header in HTTP requests

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableV1

Whether to allow clients to use the V1 API to interact with this repository

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceBasicAuth

Whether to force authentication (Docker Bearer Token Realm required if false)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpPort

Create an HTTP connector at specified port

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpsPort

Create an HTTPS connector at specified port

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProxyIndexType

Type of Docker Index

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Registry
Accept pipeline input: False
Accept wildcard characters: False
```

### -IndexUrl

Url of Docker Index to use.
Required only if ProxyIndexType is Custom

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

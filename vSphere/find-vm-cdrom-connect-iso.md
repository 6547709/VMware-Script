Get-VM | FT Name, @{Label="ISO file"; Expression = { ($_ | Get-CDDrive).ISOPath }} 



# Disconnect all CD-ROM
Get-VM | Get-CDDrive | Set-CDDrive -NoMedia -confirm:$false

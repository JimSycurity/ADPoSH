# ADPoSH
Microsoft Active Directory related PowerShell

A collection of Microsoft Active Directory PowerShell scripts and snippets.

## Active Directory Computer Object Ownership:

When using delegated permissions to join a Computer to an Active Directory domain or allowing regular users to add up to 10 devices to the domain, it is possible to have a condition where Computer Objects do not have "Domain Admins" as the object owner.  The owner of an object has the right to modify permissions on the object and read all attributes of the object.  This may allow the delegated MDT domain-join account or a standard AD user permissions to read the Computer Object's LAPS password and more.

[Get-IncorrectADComputerObjectOwner](https://github.com/JimSycurity/ADPoSH/blob/main/Get-IncorrectADComputerObjectOwner) is a 1-liner that will discover unexpected ownership of Computer Objects in AD.


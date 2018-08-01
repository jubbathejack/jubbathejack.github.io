# This is a test page
Is it on yet?

## This is some test code
```powershell
function Get-LocalAdmin {
    param (
        $strcomputer
    )
    
    $admins = Get-WmiObject win32_groupuser -computer $strcomputer
    $admins = $admins |Where-Object {$_.groupcomponent -like '*"Administrators"'}

    $admins |ForEach-Object {
        $_.partcomponent -match ".+Domain\=(.+)\,Name\=(.+)$" > $nul
        $Matches[1].trim('"') + "\" + $Matches[2].trim('"')
    }
}
```
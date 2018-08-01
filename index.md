# This is a test page
Is it on yet?

## This is some test code
This is some PowerShell code.
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

And this is some Python code
```python
name = 'Zed A. Shaw'
age = 35 # not a lie
height = 74 # inches
height_cm = height * 2.54 # Converting inches to centimeters
weight = 180 # lbs
weight_kg = weight * 0.45359237 # Converting pounds to kilograms
eyes = 'Blue'
teeth = 'White'
hair = 'Brown'

print "Let's talk about %r." % name
print "He's %d inches tall." % height
print "And that is %d centimeters tall." % height_cm
print "He's %d pounds heavy." % weight
print "And that is %d kilograms heavy." % weight_kg
print "Actually that's not too heavy."
print "He's got %s eyes and %s hair." % (eyes, hair)
print "His teeth are usually %s depending on the coffee." % teeth

# this line is tricky, try to get it exactly right
print "If I add %d, %d, and %d I get %d." % (
    age, height, weight, age + height + weight)
```
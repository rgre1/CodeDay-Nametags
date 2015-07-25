# CodeDay Nametags
CodeDay's unofficial web tool to quickly print out name tags with the Dymo Labelwriter.

Documentation
---------
The current set up was built for a [Dymo Labelwriter 450 Turbo](http://www.dymo.com/en-US/labelwriter-450-label-printer) with the use of [2-5/16 x 4 labels](http://www.dymo.com/en-US/lw-shipping-labels-2-5-16-x-4). This hasn't been tested with other Labelwriters; logically it should work.

###Other group values###
Inside of `index.html` the default group option is `Participant` which speeds up the check in process.

    <select type="select" id="typeName" name="person">
        <option value="Participant">Participant</option>
        <option value="Teacher">Teacher</option>
        <option value="Visitor">Visitor</option>
        <option value="Sponsor">Sponsor</option>
        <option value="Volunteer">Volunteer</option>
    </select>
Modify to your heart's content.

###Change the label size###
If you have other label sizes in mind, find the SKU of the selected label and it's purpose. Example: `30256 Shipping`. Where `30256` is the SKU and `Shipping` is the purpose.

Open `assets/label.xml` and hunt down 

    <PaperName>30252 Shipping</PaperName>

Replace with the appropriate values and save.

###Change the website logo###
Find `assets/logo.png` and replace. I used a 241 x 60 image but there aren't any constraints in place. 
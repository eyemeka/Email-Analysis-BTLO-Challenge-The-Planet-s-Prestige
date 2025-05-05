# Email Analysis: BTLO Challenge The Planet Prestige

# Scenario

CoCanDa, a planet known as 'The Heaven of the Universe' has been having a bad year. A series of riots have taken place across the planet due to the frequent abduction of citizens, known as CoCanDians<!--more-->, by a mysterious force. CoCanDa’s Planetary President arranged a war-room with the best brains and military leaders to work on a solution. After the meeting concluded the President was informed his daughter had disappeared. CoCanDa agents spread across multiple planets were working day and night to locate her. Two days later and there’s no update on the situation, no demand for ransom, not even a single clue regarding the whereabouts of the missing people. On the third day a CoCanDa representative, an Army Major on Earth, received an email.

# Tools and Services Used
<div>Notepad++</div>
<div>Hxd</div>
<div>Cyberchef.com</div>
<div>Graykesler.net</div>

# Step-by-Step Guide
Download the file and extract it and enter the password "btlo" all in lowercase.

Right click to open the file in Notepad++

<img class="alignnone size-full wp-image-132" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-102413.png" alt="" width="967" height="522" />



When performing email analysis, taking not of the SPF, DKIM and DMARC statues is very crucial for suspicious emails. And in this email, the SPF is set to fail

<img class="alignnone size-full wp-image-133" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-103523.png" alt="" width="1157" height="123" />

Observing the text, you will notice that the Reply To email is different from the From email. This is a very important thing to notice because where the email is coming from will be different if you want to reply to this email.

<img class="alignnone size-full wp-image-135" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-104601-1.png" alt="" width="1136" height="167" />

Below, notice the Content Type, and below that the "Content-Transfer-Encoding: base64." Decode the content below using Base64.

<img class="alignnone size-full wp-image-136" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-105346.png" alt="" width="682" height="311" />

Highlight the content, copy and log on to cybershef.com. On cyberchef.com, paste the copied content in the Input and drag <strong>From Base64</strong> and put on <strong>Recipe</strong>

<img class="alignnone size-full wp-image-137" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-110146.png" alt="" width="1591" height="683" />

Scroll down, you will see another content with <strong>Content-Type: application/pdf; name="PuzzleToCoCanDa.pdf</strong>.

This will most likely be the attachment mentioned in the body of the email. The content transfer type is also encoded with base46 (Content-Transfer-Encoding: base64)

<img class="alignnone size-full wp-image-138" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-111341.png" alt="" width="680" height="389" />
<div>Copy the content and paste it again in Cyberchef.com in another tab. Before saving this file, convert it to Hexadecimal by  dragging the To Hex into the Recipe to see what the Output of the content will be. Blow is the result.</div>
<div></div>
<div></div>
<div><img class="alignnone size-full wp-image-139" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-112252.png" alt="" width="1585" height="498" /></div>
<div></div>
<div>
<div>The reason for this is because is if we look at the first few numbers <strong>50 4b 03 14 04. </strong>The first number of bits of a file makes up a file signature (file header aka magic number).</div>
<div></div>
<div>And because the file name <strong>PuzzleToCoCanDa.pdf</strong> does not mean it is really a PDF file. It is important to look at the file signature or file header to really determine what that file really is.</div>
</div>
<div></div>
<div>Copy the first couple of numbers of bits (50 4b 03 14 04). Log on to google.com and search for Gary Kesler file signature, choose the garykesler.net.</div>
<div></div>
<div><img class="alignnone size-full wp-image-140" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-114108.png" alt="" width="1556" height="512" /></div>
<div></div>
<div>Once you are on the page, press <strong>Ctrl+F </strong> and paste the number or bits you copied earlier</div>
<div></div>
<div><img class="alignnone size-full wp-image-141" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-114655.png" alt="" width="1088" height="242" /></div>
<div></div>
<div>Notice it says the first number or bits is a ZIP extension but from the email it says PDF</div>
<div></div>
<div>Now go back to cyberchef, remove the To Hex, and allow it to to return to the normal output from the Base64 and save it as Attachment.zip</div>
<div><img class="alignnone size-full wp-image-142" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-115348.png" alt="" width="1082" height="470" /></div>
<div></div>
<div>Extract the Attachment.zip file, among the files extracted. In case there are hidden files, click on View, and uncheck hidden item and you will notice Money.xlsx Excel Sheet.</div>
<div></div>
<div>Open your Hxd and drag the first file into it, and copy the first bits (FF D8 FF E0)</div>
<div><img class="alignnone size-full wp-image-143" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-121213.png" alt="" width="614" height="180" /></div>
<div></div>
<div>Head back to Graykesler.net and paste the bits. As you can see below, the first few bits relates to JPEG, JPG file</div>
<div><img class="alignnone size-full wp-image-144" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-121523.png" alt="" width="958" height="103" /></div>
<div></div>
<div>Go back to the file and rename it and add a .JPEG to it and when you double click it, it looks like this, a crown</div>
<div><img class="alignnone size-full wp-image-145" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-122115.png" alt="" width="948" height="537" /></div>
<div></div>
<div></div>
<div>Repeat the same thing for the second file (GoodJobMajor). Drag into a new Hxd file and copy the first bits (25 50 44 46), go to Graykesler.net. You will notice this is a PDF file. Return to the file ad rename it by adding . PDF (GoodJobMajor.pdf)</div>
<div></div>
<div><img class="alignnone size-full wp-image-146" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-122721.png" alt="" width="809" height="520" /></div>
<div></div>
<div>The third file is the Money.xlsx file. You can open that using your Excel sheet. In the Excel sheet you will notice that there are Sheet 1 and Sheet 3. Sheet one messages are in plain text as you can see below</div>
<div><img class="alignnone size-full wp-image-147" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-161449.png" alt="" width="586" height="160" /></div>
<div></div>
<div>But the sheet 3 appears to be blank at first, since this is a CTF challange, there might be hidden message in white text so right click and clear text format to see the message.</div>
<div><img class="alignnone size-full wp-image-149" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-162131.png" alt="" width="725" height="141" /></div>
<div></div>
<div>The message is in Base64, copy and log on to cyerchef again, paste in input and convert from Base64. See below</div>
<div><img class="alignnone size-full wp-image-150" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-162301.png" alt="" width="1323" height="493" /></div>
<div></div>
<div>Time to answer some question...</div>
<div></div>
<div>

# Challenge Submission
<em><strong>What is the email service used by the malicious actor? (1 points)</strong></em>

<img class="alignnone size-full wp-image-151" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-163328.png" alt="" width="815" height="96" />

<em>Emkei.cz</em>

<em><strong>What is the Reply-To email address? (2 points)</strong></em>

<img class="alignnone size-full wp-image-152" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-164013.png" alt="" width="915" height="109" />

<em>negeja3921@pashter.com</em>

<em><strong>What is the filetype of the received attachment</strong> </em>

From out analysis we discovered that the PDF file was not a PDF but was a .ZIP file

<em>.zip</em>

<em><strong>What is the name of the malicious actor? (2 points)</strong></em>

To get the Meta Data of the Attachment.zip file, use ExifTool for your Windows machine.

<em>Pestero Negeja</em>

<em><strong>What is the location of the attacker in this Universe? (2 points)</strong></em>

We got this after converting from Base64 to plaintext in cyberchef in the Money.xlsx Excel Sheet, Sheet 3

<em>The Martian Colony, Beside Interplanetary Spaceport</em>

<em><strong>What could be the probable C&amp;C domain to control the attacker’s autonomous bots? (2 points)</strong></em>

From the text editor, we see the Reply To

<img class="alignnone size-full wp-image-154" src="https://eyemekacyberportfolio.name.ng/wp-content/uploads/2025/04/Screenshot-2025-04-18-173125.png" alt="" width="676" height="107" />

</div>
<div><em>pashter.com</em></div>

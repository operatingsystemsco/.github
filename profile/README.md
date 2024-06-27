<img src="./images/github-header-image.png">


How to Build MS-DOS and the Windows Operating System
				
<p><a target="_self" href="https://computerhistory.org/blog/microsoft-ms-dos-early-source-code/" data-test-app-aware-link="">MS-DOS Source</a></p>
<p>MS-DOS 1.25 was published on GitHub MS-DOS 1.25 was completely written in 8086 assembly so it needs to be assembled using an assembler (MASM and SCP 8086 Assembler). The object file(s) produced by MASM will then be linked to produce an executable which will then be converted to a raw binary executable (.COM). The .HEX files produced by SCP 8086 Assembler will be converted directly to raw .COM files using the HEX2BIN utility.</p>
<p>2. How to Make DOS?</p>

<p>This is as hard as the source code for the DOS BIOS (IO.SYS) was designed for Virtual Box and is not PC-compatible. Theoretically, the compiled binaries should work on Virtual Box but using the source code release by Microsoft alone will not produce a valid bootable disk as no source code for the boot sector is given. I do have access to the source code of the boot sector but as a result of Microsoft not releasing it publicly, I will not share it. This basically means with only the source code published by Microsoft, it is impossible to produce a working copy of MS-DOS 1.25.</p>
<p>3. What is Required</p>

<p>The following is required for compiling MS-DOS 1.25:</p>
<ul>
   <li> Microsoft Macro Assembler (MASM)</li>
   <li> Microsoft 8086 Object Linker (LINK)</li>
   <li> EXE to Binary Conversion Utility (EXE2BIN)</li>
   <li> Seattle Computer Products 8086 Assembler (ASM)</li>
   <li> HEX to Binary Conversion Utility (HEX2BIN)</li>
   <li> A copy of the MS-DOS 1.25 source code</li>
</ul>
<p>4. Details</p>

<p>The files STDDOS.ASM and MSDOS.ASM can be assembled to produce the DOS kernel and they are MASM compatible. All switches are set in the file STDDOS.ASM. MSVER generates binaries for MS-DOS with Microsoft copyright strings, IBM produces IBM PC-DOS binaries with IBM copyright strings. There is no need to change HIMEM and DSKTEST unless you want to experiment more with it.</p>

<p>COMMAND.ASM can be assembled using MASM to produce the command interpreter for MS-DOS. Just like the DOS kernel, you may use switches to produce both MS-DOS and IBM PC-DOS binaries. The HIMEM switch is also present.</p>

<p>ASM.ASM, HEX2BIN.ASM, IO.ASM and TRANS.ASM were written by SCP and must be assembled using their own assembler. IO.ASM have switches to configure the floppy disk controller and the Cromemco 4FDC is currently supported by The SIMH Altair 8800 Z80 simulator.</p>
<p>5. Compile It</p>

<p>Now, we are ready to compile MS-DOS 1.25 for the first time! If you are experienced in assembly, used those assemblers and tools listed above, then you should be able to get everything done by yourself. For those unable to assemble it on their own, my build disk will save your time.</p>

<p>Here is how to build MS-DOS 1.25 with the build disk: Download the build disk. Create a new virtual machine using your favorite emulator or hypervisor. Add a floppy drive, load the build disk. Start the virtual machine (it should boot from the build disk). Check the filenames using the DIR command and it should return: Type in MK <FILENAME> to assemble that particular component or MK ALL to assemble everything. Once you have everything assembled, type in DIR *.COM and DIR *.SYS to see the executable produced, it should be similar to: You have done it! You can now copy those executables to another disk or extract them or run them!
</p>
<p>After reading a Windows Open Source Article Mark Russivich said it wold take a rocket scientist to build Microsoft Windows and I have. I at leas thold my almatrer to that.</p>
<li><a target="_self" href="https://www.wired.com/2015/04/microsoft-open-source-windows-definitely-possible/">Microsoft: An Open Source Windows Is 'Definitely Possible'</a></li>

<h2>Please Sign the Sphinx Logic and Microsoft CLA<h2>
<ul>
<li><a target="_self" href="https://opensource.microsoft.com/cla/">Microsoft CLA</a></li>
<li><a target="_self" href="https://cla-assistant.io/">Sphinx Logic CLA</a></li>
<li><a target="_self" href="https://betawiki.net/wiki/Build_lab">Build Lab --with Microsoft Employees</a></li>
</ul>

<h2>Acedemia</h2>
<ul>
<li><a target="_self" href="https://www.psychologytoday.com/us/blog/biocentrism/201112/does-the-soul-exist-evidence-says-yes" data-test-app-aware-link="">Does the Soul Exist? Evidence Says ‘Yes’</a></li> 
<li><a href="https://news.okstate.edu/magazines/research/research-matters/articles/2017/poetry-building-blocks-engineering.html">Poetry as the building blocks of engineering</a></li>
<li><a href="https://www.minix3.org/" data-test-app-aware-link="">MINX 3</a></li>
<li><a target="_self" href="https://ocw.oouagoiwoye.edu.ng/about/mirror-site-program/">MIT Open Courseware Mirror Site Program</a></li>
<li><a target="_self" href="https://github.com/sphinxlogic/Biography">My Biography -- Work in Progress</a></li>
<li><a target="_self" href="https://scholar.google.com/citations?user=aBc-Oc8AAAAJ&hl=en">My Google Scholar</a></li>
<li><a target="_self" href="https://www.goodreads.com/jonathandavidmoore">My Goodreads</a></li>
<li><a target="_self" href="https://www.imdb.com/user/ur154049466/watchlist/">My IMDB</a></li>
<li><a target="_self" href="https://futuretimeline.net/">Future Timeline</a></li> 
<li><a target="_self" href="https://www.theverge.com/2021/6/5/22491859/supreme-court-van-buren-cfaa-hacking-law-scope-narrowed">The Supreme Court pared down a controversial anti-hacking law</a></li>
</ul>

<h2>Progress</h2>
<ul>
<li><a href="https://plato.stanford.edu/entries/progress/">Progress</a></li>
<li><a href="https://www.smithsonianmag.com/smart-news/pope-would-you-accept-evolution-and-big-bang-180953166/">The Pope Would Like You to Accept Evolution and the Big Bang</a></li>
<li><a href="https://www.sciencedirect.com/science/article/abs/pii/S0924933810701140">The philosophical understanding of schizophrenia</a></li>
</ul>

<h2>Architecure</h2>
<ul>
<li><a href="https://en.wikipedia.org/wiki/X86-64">X86-64</a></li>
</ul>

<p>According to Andrew Tanumbuam top down Operating System design is best, bottom up is more practical.</p>

<h2>My Visual Studio Extension in the Makrketplace</h2>

<p><a href="https://marketplace.visualstudio.com/items?itemName=jdm7dv1.JSEnrichments">Javascript Essentials</a></li>

<h2>Relgious Views of Charles Darwin</h2>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Religious_views_of_Charles_Darwin">Reigious Views of Chareles Darwin</a></li>
<li><a href="https://abcnews.go.com/Technology/story?id=5817850&page=1">Anglican clergyman: Church owes Darwin an apology</a></li>
</ul>

<h2>Ecology</h2>
<ul>
<li><a href="https://pubmed.ncbi.nlm.nih.gov/3493534/">Disease competition as a factor in ecological studies</a></li>
</ul>

<h2>History of Microsoft</h2>
<ul>
<li><a href="https://en.wikipedia.org/wiki/History_of_Microsoft">History of Microsoft</a></li>
<li><a href="https://learn.microsoft.com/en-us/shows/history/history-of-microsoft-1993">The History of Microsoft - 1993</a></li>
</ul>
<p>I started in 1982 with a TRS-80 Computer Limited Edtion one of a kind and Microsoft XEINX and TR-DOS, I've beed Sleepless in Seattle since 1992 and Singles the Movie</p>

<h2>History of Microsoft UNIX Licensing and Corporate Darwnism.</h2>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Santa_Cruz_Operation">Santa Cruz Operation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Classic_Mac_OS">Classic Mac OS</a></li>
<li><a href="https://en.wikipedia.org/wiki/DEC_MICA">Digital Corp's MICA</a></li>
</ul>

<h2>Microsoft Agreements</h2>
<ul>
<li><a href="https://news.microsoft.com/2002/02/21/microsoft-announces-major-expansion-of-shared-source-initiativeproviding-source-code-to-systems-integrators/">Microsoft Announces Major Expansion of Shared Source Initiative,Providing Source Code to Systems Integrators</a></li>
<li><a href="https://news.microsoft.com/2002/03/27/microsoft-releases-shared-source-cli-and-c-implementation/">Microsoft Releases Shared Source CLI and C# Implementation</a></li>
<li><a href="https://www.cnet.com/tech/tech-industry/commentary-shared-source-needs-commitment/">Commentary: Shared source needs commitment</a></li>
<li><a href="https://www.microsoft.com/licensing/docs/view/Products/Software-products">Licencing Documents</a></li>
<li><a href="https://learn.microsoft.com/en-us/azure/cost-management-billing/manage/create-enterprise-subscription?WT.mc_id=facebook">Create a Enterprise Agreement Subscription.</a></li>
<li><a href="https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/design-area/azure-billing-enterprise-agreement">Plan for Enterprise Agreement enrollment</a></li>
<li><a href="https://learn.microsoft.com/en-us/azure/cost-management-billing/manage/ea-direct-portal-get-started">Get started with your Enterprise Agreement billing account</a></li>
<li><a href="https://www.microsoft.com/en-us/sharedsource/enterprise-source-licensing-program.aspx">Enterprise Source Licensing Program</a></li>
<li><a href="https://azure.microsoft.com/en-us/pricing/offers/ms-azr-0111p">Azure in Open</a></li>
<li><a href="https://learn.microsoft.com/en-us/visualstudio/subscriptions/buy-activate-retail">Visual Studio subscriptions are available through the Microsoft Store</a></li>
<li><a href="https://marketplace.visualstudio.com/vs">Extensions for Visual Studio & Subscriptions</a></li>
<li><a href="https://learn.microsoft.com/en-us/partner-center/mpn-get-action-pack">Microsoft Action Pack Subscription (MAPS)</a></li>
<li><a href="https://learn.microsoft.com/en-us/lifecycle/products/windows-10-enterprise-ltsc-2019">Windows 10 Enterprise LTSC 2019</a>
<li>You must own a Enterprise Product to have a Enterprise Agreement with a EULA and at least 5 PC's</li>
</ul>

<h2>Microsoft's Open Source Program</h2>
<ul>
<li><a href="https://opensource.microsoft.com/program/">Open Source Program</a></li>
<li><a href="https://learn.microsoft.com/en-us/openspecs/dev_center/ms-devcentlp/13571077-e344-4e6f-a477-369894979798">Patent Promises and Patents</a></li>
</ul>

<h2>Adobe Contibutor Licence Agreement</h2>
<ul>
<li><a href="https://opensource.adobe.com/cla.html">Adobe Open Source</a></li>
</ul>

<h2>Microsoft Legal</h2>
<ul>
<li><a href="https://learn.microsoft.com/en-us/entra/identity/saas-apps/convercent-tutorial">Tutorial: Microsoft Entra integration with Convercent</a></li>
</ul>

<h2>Finance</h2>
<ul>
<li><a href="https://www.lawinsider.com/dictionary/liquidity-value">Liquidity Value definition</a></li>
<li><a href="https://www.investopedia.com/terms/n/noi.asp">Net Operating Income For Real Estate</a></li>
<li><a href="https://www.investopedia.com/terms/d/dscr.asp">Debt-Service Coverage Ratio</a></li>
<li><a href="https://www.tandfonline.com/doi/pdf/10.1080/00036847200000037">Patents, profitability, liquidity and firm size</a></li>
<li><a href="https://www.investopedia.com/terms/c/capital.asp">Capital: Definition, How It's Used, Structure, and Types in Business</a></li>
<li><a href="https://www.lawinsider.com/clause/cash-out">Cash Out Samples Clauses</a></li>
<li><a href="https://content.next.westlaw.com/practical-law/document/I3f4a4679e8db11e398db8b09b4f043e0/Power-of-advancement?viewType=FullText&transitionType=Default&contextData=(sc.Default)">Power of Advancment</a></li>  
<li><a href="https://www.investopedia.com/terms/c/cashequivalents.asp">What Are Cash Equivalents? Types, Features, Examples</a></li> 
<li><a href="https://www.lawinsider.com/clause/cash-consideration">Cash Consideration</a></li> 
</ul>

<h2>Industry Links</h2>
<ul>
<li><a target="_self" href="https://www.zdnet.com/article/why-microsoft-is-turning-into-an-open-source-company/">Why Microsoft is turning into an open-source company</a></li>
<li><a target="_self" href="https://en.wikipedia.org/wiki/DECUS" data-test-app-aware-link="">DECUS</a></li>
<li><a target="_self" href="https://www.itprotoday.com/compute-engines/mipsnt-allied-birth" data-test-app-aware-link="">MIPS/NT allied at birth</a></li> 
<li><a target="_self" href="https://www.itprotoday.com/compute-engines/windows-nt-and-vms-rest-story" data-test-app-aware-link="">Windows NT and VMS: The Rest of the Story</a></li>
<li><a target="_self" href="https://www.computerworld.com/article/1727355/sco-confirms-microsoft-has-licensed-its-unix-technology.html" data-test-app-aware-link="">SCO confirms Microsoft has licensed its Unix technology</a></li>
<li><a target="_self" href="https://www.wired.com/1997/11/microsoft-settles-fight-with-santa-cruz/" data-test-app-aware-link="">Microsoft Settles Fight with Santa Cruz Operation</a></li>
<li><a target="_self" href="https://news.microsoft.com/2006/11/02/microsoft-and-novell-announce-broad-collaboration-on-windows-and-linux-interoperability-and-support/" data-test-app-aware-link="">Microsoft and Novell Announce Broad Collaboration on Windows and Linux Interoperability and Support</a></li>
<li><a target="_self" href="https://learn.microsoft.com/en-us/visualstudio/releases/2019/compatibility" data-test-app-aware-link="">Visual Studio 2019 Compatibility</a></li>
<li><a target="_self" href="https://devblogs.microsoft.com/oldnewthing/20180122-00/?p=97855" data-test-app-aware-link="">The history of change-packing tools at Microsoft (so far)</a></li>
<li><a target="_self" href="https://devblogs.microsoft.com/oldnewthing/20181224-00/?p=100545" data-test-app-aware-link="">Random internal Windows terminology: IDW, Razzle, and their forgotten partners IDS and Dazzle</a></li>
<li><a target="_self" href="https://cybersecurity.att.com/blogs/security-essentials/its-only-a-hacker-if-its-linus-himself" data-test-app-aware-link="">It's Only A Hacker If It's Linus Himself</a></li>
<li><a target="_self" href="https://www.zdnet.com/article/minix-intels-hidden-in-chip-operating-system/" data-test-app-aware-link="">MINIX: ​Intel's hidden in-chip operating system</a></li>
<li><a href="https://devclass.com/2023/05/25/azure-linux-released-at-build-where-microsoft-revealed-why-it-did-not-fork-fedora/">Azure Linux released at Build where Microsoft revealed why it did not fork Fedora</a></li></ul>
</ul>


<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1 plus MathML 2.0//EN"
        "HTMLFiles/xhtml-math11-f.dtd">

<!-- Created with the Wolfram Language : www.wolfram.com -->

<html xmlns="http://www.w3.org/1999/xhtml">
<head>
 <title>
  CVHW5
 </title>
 <link href="HTMLFiles/CVHW5.css" rel="stylesheet" type="text/css" />
</head>

<body>

<p class="Title">
 The 5th homework.
</p>



<p class="Text">
 No.2160508170
</p>



<p class="Section">
 Image Preprocessing
</p>



<p class="Subsection">
 Import the images
</p>



<p class="Code">
 <img src="HTMLFiles/CVHW5_1.gif" alt="CVHW5_1.gif" width="866" height="84" style="vertical-align:middle" />
</p>

<table class='Output'>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>Test image 0</span></td>
  <td style='text-align: center;'><span>Test image 1</span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_2.gif" alt="CVHW5_2.gif" width="180" height="101" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_3.gif" alt="CVHW5_3.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
 </tr>
</table>

<p class="Subsection">
 Scale the input pictures to 256*256;<br />Pad them into 512*512;<br />Centralize the spectrum.
</p>



<p class="Text">
 The centralization of the spectrum is performed by multiplying <span><span><img src="HTMLFiles/CVHW5_4.png" alt="CVHW5_4.png" width="50" height="20" style="vertical-align:middle" /></span></span> pixel by pixel. Proof:
</p>



<p class='Text' style='text-align: left;'>
 <span class="TextInline"><span><img src="HTMLFiles/CVHW5_5.gif" alt="CVHW5_5.gif" width="283" height="210" style="vertical-align:middle" /></span></span>
</p>



<p class="Text">
 
</p>



<p class="Code">
 <img src="HTMLFiles/CVHW5_6.gif" alt="CVHW5_6.gif" width="630" height="173" style="vertical-align:middle" />
</p>

<table class='Output'>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>Preprocessing Result</span></td>
  <td style='text-align: center;'><span></span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>Image0</span></td>
  <td style='text-align: center;'><span>Image1</span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_7.gif" alt="CVHW5_7.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_8.gif" alt="CVHW5_8.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
 </tr>
</table>

<p class="Subsection">
 The Fourier Spectrum before Processing:
</p>



<p class="Code">
 <img src="HTMLFiles/CVHW5_9.gif" alt="CVHW5_9.gif" width="1157" height="62" style="vertical-align:middle" />
</p>

<table class='Output' frame='box'>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>The raw image</span></td>
  <td style='text-align: center;'><span>Periodogram</span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_10.gif" alt="CVHW5_10.gif" width="180" height="101" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_11.gif" alt="CVHW5_11.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_12.gif" alt="CVHW5_12.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_13.gif" alt="CVHW5_13.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
 </tr>
</table>

<p class="Section">
 <span class="SectionInline">Butterworth LPF</span>
</p>



<p class="Text">
 Butterworth filter is type of FIR filter designed to have a frequency response as flat as possible in the passband. The frequency response of the Butterworth LPF is:
</p>



<p class='Text' style='text-align: left;'>
 <span><span><img src="HTMLFiles/CVHW5_14.png" alt="CVHW5_14.png" width="210" height="91" style="vertical-align:middle" /></span></span>
</p>



<p class="Text">
 To solve the exact transfer function of the filter, we rewrite the G(&omega;) into <span><span><img src="HTMLFiles/CVHW5_15.png" alt="CVHW5_15.png" width="281" height="78" style="vertical-align:middle" /></span></span>. Noting that the polarization must lie in the region where Re{s} &lt; 0, the H(&omega;) can be solved<br />Engineers suffers to calculate the transfer function again and again and some of them summerize the standardized function and make a table. 
</p>



<p class="Code">
 <img src="HTMLFiles/CVHW5_16.png" alt="CVHW5_16.png" width="704" height="17" style="vertical-align:middle" />
</p>

<table class='Output' frame='box' rules='all'>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>1</span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_17.gif" alt="CVHW5_17.gif" width="79" height="46" style="vertical-align:middle" /></span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>2</span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_18.gif" alt="CVHW5_18.gif" width="138" height="49" style="vertical-align:middle" /></span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>3</span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_19.gif" alt="CVHW5_19.gif" width="163" height="49" style="vertical-align:middle" /></span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>4</span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_20.gif" alt="CVHW5_20.gif" width="741" height="53" style="vertical-align:middle" /></span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>5</span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_21.gif" alt="CVHW5_21.gif" width="305" height="49" style="vertical-align:middle" /></span></td>
 </tr>
</table>

<p class="Text">
 Substituting the &omega; into <span><span><img src="HTMLFiles/CVHW5_22.png" alt="CVHW5_22.png" width="91" height="46" style="vertical-align:middle" /></span></span> yields the 2D Butterworth LPF.
</p>



<p class="Input">
 <img src="HTMLFiles/CVHW5_23.png" alt="CVHW5_23.png" width="4" height="18" style="vertical-align:middle" />
</p>

<p class="Subsection">
 Generate Butterworth 1D Low-pass Filters
</p>



<p class="Text">
 <br /><span style='font-size: 36px;color: #FF0000;'>It&rsquo;s not a wise choice to copy the formula from the test book because it&rsquo;s simply wrong.</span><span style='font-size: 36px;'><br /></span> The author mistake the <span><span><img src="HTMLFiles/CVHW5_24.png" alt="CVHW5_24.png" width="64" height="20" style="vertical-align:middle" /></span></span> and the ||H(&omega;)||, and yielding a wrong cutoff frequency.<br /> <br /> We construct the LPF from the continuous version Butterworth LPF prototype and then convert the continuous LPF into discrete LPF. Thus, three parameters are to be determined: the cutoff frequency <span><span><img src="HTMLFiles/CVHW5_25.png" alt="CVHW5_25.png" width="19" height="20" style="vertical-align:middle" /></span></span>,the order of the LPF n and the sampling interval &tau;. <br /> The final cutoff frequency <span><span><img src="HTMLFiles/CVHW5_26.png" alt="CVHW5_26.png" width="18" height="20" style="vertical-align:middle" /></span></span> in DFT is :
</p>



<p class='Text' style='text-align: left;'>
 <span><span><img src="HTMLFiles/CVHW5_27.png" alt="CVHW5_27.png" width="149" height="44" style="vertical-align:middle" /></span></span>
</p>



<p class="Text">
 The possible error lies in the sampling and DFT procedure. Frequency leakage result in the deviation of the cutoff frequency. The higher cutoff frequency, the higher error.
</p>



<p class="Code">
 <img src="HTMLFiles/CVHW5_28.gif" alt="CVHW5_28.gif" width="1069" height="379" style="vertical-align:middle" />
</p>

<p class="Print">
 <img src="HTMLFiles/CVHW5_29.png" alt="CVHW5_29.png" width="250" height="17" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/CVHW5_30.gif" alt="CVHW5_30.gif" width="360" height="225" style="vertical-align:middle" />
</p>

<p class="Print">
 <img src="HTMLFiles/CVHW5_31.png" alt="CVHW5_31.png" width="383" height="17" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/CVHW5_32.gif" alt="CVHW5_32.gif" width="360" height="241" style="vertical-align:middle" />
</p>

<p class="Subsection">
 Generate 2D Butterworth FIlter
</p>



<p class="Code">
 <img src="HTMLFiles/CVHW5_33.gif" alt="CVHW5_33.gif" width="907" height="179" style="vertical-align:middle" />
</p>

<p class="Message">
 <img src="HTMLFiles/CVHW5_34.png" alt="CVHW5_34.png" width="772" height="14" style="vertical-align:middle;" usemap="#map_34" />
<map name="map_34">
<area shape="rect" coords="0,14,20,0" title="Dynamic[RawBoxes[FEPrivate`FrontEndResource[FEStrings, messageMenuTooltip]]]" nohref="" />
</map>
</p>

<table class='Output'>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span></span></td>
  <td style='text-align: center;'><span>The 2D butterworth filter</span></td>
  <td style='text-align: center;'><span></span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>Periodogram</span></td>
  <td style='text-align: center;'><span>3D View</span></td>
  <td style='text-align: center;'><span>CounterPlot</span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_35.gif" alt="CVHW5_35.gif" width="256" height="256" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_36.gif" alt="CVHW5_36.gif" width="360" height="286" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_37.gif" alt="CVHW5_37.gif" width="360" height="357" style="vertical-align:middle;" usemap="#map_37" />
<map name="map_37">
<area shape="rect" coords="93,266,285,74" title="0.2" nohref="" />
<area shape="rect" coords="98,261,279,80" title="0.4" nohref="" />
<area shape="rect" coords="102,257,276,83" title="0.6" nohref="" />
<area shape="rect" coords="104,255,274,85" title="0.8" nohref="" />
<area shape="rect" coords="106,253,272,87" title="1" nohref="" />
<area shape="rect" coords="108,251,270,89" title="1.2" nohref="" />
<area shape="rect" coords="110,249,268,91" title="1.4" nohref="" />
<area shape="rect" coords="112,247,266,93" title="1.6" nohref="" />
<area shape="rect" coords="115,244,263,96" title="1.8" nohref="" />
<area shape="rect" coords="172,187,206,153" title="2" nohref="" />
</map></span></td>
 </tr>
</table>

<p class="Section">
 <span class="SectionInline">Gaussian LPF</span>
</p>



<p class="Subsubsection">
 <span class="SubsectionInline">Generate the Gaussian Filter</span>
</p>



<p class="Code">
 <img src="HTMLFiles/CVHW5_38.gif" alt="CVHW5_38.gif" width="883" height="150" style="vertical-align:middle" />
</p>

<table class='Output'>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span></span></td>
  <td style='text-align: center;'><span>The 2D gaussian filter</span></td>
  <td style='text-align: center;'><span></span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>Periodogram</span></td>
  <td style='text-align: center;'><span>3D View</span></td>
  <td style='text-align: center;'><span>CounterPlot</span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_39.gif" alt="CVHW5_39.gif" width="256" height="256" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_40.gif" alt="CVHW5_40.gif" width="360" height="286" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_41.gif" alt="CVHW5_41.gif" width="360" height="357" style="vertical-align:middle;" usemap="#map_41" />
<map name="map_41">
<area shape="rect" coords="49,310,328,31" title="0.2" nohref="" />
<area shape="rect" coords="72,287,306,53" title="0.4" nohref="" />
<area shape="rect" coords="87,272,291,68" title="0.6" nohref="" />
<area shape="rect" coords="100,259,278,81" title="0.8" nohref="" />
<area shape="rect" coords="111,248,267,92" title="1" nohref="" />
<area shape="rect" coords="121,238,256,103" title="1.2" nohref="" />
<area shape="rect" coords="132,227,246,113" title="1.4" nohref="" />
<area shape="rect" coords="143,216,234,125" title="1.6" nohref="" />
<area shape="rect" coords="156,203,221,138" title="1.8" nohref="" />
</map></span></td>
 </tr>
</table>

<p class="Section">
 LPF Filter Test
</p>



<p class="Code">
 <img src="HTMLFiles/CVHW5_42.gif" alt="CVHW5_42.gif" width="1173" height="260" style="vertical-align:middle" />
</p>

<table class='Output'>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>Raw</span></td>
  <td style='text-align: center;'><span>Butterworth</span></td>
  <td style='text-align: center;'><span>Gaussian</span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_43.gif" alt="CVHW5_43.gif" width="180" height="101" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_44.gif" alt="CVHW5_44.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_45.gif" alt="CVHW5_45.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_46.gif" alt="CVHW5_46.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_47.gif" alt="CVHW5_47.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_48.gif" alt="CVHW5_48.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
 </tr>
</table>

<p class="Section">
 Butterworth HPF
</p>



<p class="Subsection">
 Generate Butterworth 1D Low-pass Filters
</p>



<p class="Code">
 <img src="HTMLFiles/CVHW5_49.gif" alt="CVHW5_49.gif" width="1069" height="379" style="vertical-align:middle" />
</p>

<p class="Print">
 <img src="HTMLFiles/CVHW5_50.png" alt="CVHW5_50.png" width="250" height="17" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/CVHW5_51.gif" alt="CVHW5_51.gif" width="360" height="229" style="vertical-align:middle" />
</p>

<p class="Print">
 <img src="HTMLFiles/CVHW5_52.png" alt="CVHW5_52.png" width="383" height="17" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/CVHW5_53.gif" alt="CVHW5_53.gif" width="360" height="236" style="vertical-align:middle" />
</p>

<p class="Subsection">
 Generate the 2D Butterworth HPF
</p>



<p class="Code">
 <img src="HTMLFiles/CVHW5_54.gif" alt="CVHW5_54.gif" width="868" height="179" style="vertical-align:middle" />
</p>

<p class="Message">
 <img src="HTMLFiles/CVHW5_55.png" alt="CVHW5_55.png" width="772" height="14" style="vertical-align:middle;" usemap="#map_55" />
<map name="map_55">
<area shape="rect" coords="0,14,20,0" title="Dynamic[RawBoxes[FEPrivate`FrontEndResource[FEStrings, messageMenuTooltip]]]" nohref="" />
</map>
</p>

<table class='Output'>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span></span></td>
  <td style='text-align: center;'><span>The 2D butterworth filter</span></td>
  <td style='text-align: center;'><span></span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>Periodogram</span></td>
  <td style='text-align: center;'><span>3D View</span></td>
  <td style='text-align: center;'><span>CounterPlot</span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_56.gif" alt="CVHW5_56.gif" width="256" height="256" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_57.gif" alt="CVHW5_57.gif" width="360" height="286" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_58.gif" alt="CVHW5_58.gif" width="360" height="357" style="vertical-align:middle;" usemap="#map_58" />
<map name="map_58">
<area shape="rect" coords="184,175,193,166" title="0" nohref="" />
<area shape="rect" coords="181,178,197,162" title="0.25" nohref="" />
<area shape="rect" coords="178,181,200,159" title="0.5" nohref="" />
<area shape="rect" coords="174,185,204,155" title="0.75" nohref="" />
<area shape="rect" coords="169,190,208,151" title="1" nohref="" />
<area shape="rect" coords="164,195,214,145" title="1.25" nohref="" />
<area shape="rect" coords="155,204,222,137" title="1.5" nohref="" />
<area shape="rect" coords="138,221,239,120" title="1.75" nohref="" />
</map></span></td>
 </tr>
</table>

<p class="Section">
 Gaussian HPF.
</p>



<p class="Code">
 <img src="HTMLFiles/CVHW5_59.gif" alt="CVHW5_59.gif" width="883" height="172" style="vertical-align:middle" />
</p>

<table class='Output'>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span></span></td>
  <td style='text-align: center;'><span>The 2D gaussian filter</span></td>
  <td style='text-align: center;'><span></span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>Periodogram</span></td>
  <td style='text-align: center;'><span>3D View</span></td>
  <td style='text-align: center;'><span>CounterPlot</span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_60.gif" alt="CVHW5_60.gif" width="256" height="256" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_61.gif" alt="CVHW5_61.gif" width="360" height="286" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_62.gif" alt="CVHW5_62.gif" width="360" height="357" style="vertical-align:middle;" usemap="#map_62" />
<map name="map_62">
<area shape="rect" coords="174,185,204,155" title="-0.8" nohref="" />
<area shape="rect" coords="169,190,209,150" title="-0.6" nohref="" />
<area shape="rect" coords="164,195,213,146" title="-0.4" nohref="" />
<area shape="rect" coords="160,199,218,141" title="-0.2" nohref="" />
<area shape="rect" coords="156,203,222,137" title="0" nohref="" />
<area shape="rect" coords="151,208,226,133" title="0.2" nohref="" />
<area shape="rect" coords="146,213,231,128" title="0.4" nohref="" />
<area shape="rect" coords="140,219,238,121" title="0.6" nohref="" />
<area shape="rect" coords="131,228,247,112" title="0.8" nohref="" />
<area shape="rect" coords="24,335,354,5" title="1" nohref="" />
</map></span></td>
 </tr>
</table>

<p class="Section">
 HPF Test
</p>



<p class="Code">
 <img src="HTMLFiles/CVHW5_63.gif" alt="CVHW5_63.gif" width="1770" height="150" style="vertical-align:middle" />
</p>

<table class='Output'>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span>Raw</span></td>
  <td style='text-align: center;'><span>Butterworth</span></td>
  <td style='text-align: center;'><span>Gaussian</span></td>
  <td style='text-align: center;'><span>Laplacian</span></td>
  <td style='text-align: center;'><span>USM</span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_64.gif" alt="CVHW5_64.gif" width="180" height="101" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_65.gif" alt="CVHW5_65.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_66.gif" alt="CVHW5_66.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_67.gif" alt="CVHW5_67.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_68.gif" alt="CVHW5_68.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
 </tr>
 <tr style='vertical-align: baseline;'>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_69.gif" alt="CVHW5_69.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_70.gif" alt="CVHW5_70.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_71.gif" alt="CVHW5_71.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_72.gif" alt="CVHW5_72.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
  <td style='text-align: center;'><span><img src="HTMLFiles/CVHW5_73.gif" alt="CVHW5_73.gif" width="180" height="180" style="vertical-align:middle" /></span></td>
 </tr>
</table>




<div style="font-family:Helvetica; font-size:11px; width:100%; border:1px none #999999; border-top-style:solid; padding-top:2px; margin-top:20px;">
 <a href="http://www.wolfram.com/language/" style="color:#000; text-decoration:none;">
  <span style="color:#555555">Created with the Wolfram Language</span> 
 </a>
</div>
</body>

</html>

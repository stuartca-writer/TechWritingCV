# Software Writing Examples



###

## Advantech software

This is an example of a piece of software used by Advantech customers.

\
**Software used:**\
Adobe Framemaker\
SnagIt

**Import APAX-5000/6000 Variables**

WebAccess supports the importing of Advantech APAX-5000 and 6000 series variables, including Tag names and Tag addresses, from the KW CSV file to the WebAccess database and automatically converts the KW variable address to a Modbus address for runtime exchange real-time data.

![](.gitbook/assets/0.png)

### Step 1：APAX KW CSV Configuration

When you make all the IO configurations and variable settings, execute the following instructions to export all the variables (Global Variables only):

Select **File** and **Export**：Export the I/O information to the CSV file from the command line.

![Figure 19.4.1：KW page](.gitbook/assets/1.jpeg)



Select **Cross reference** from the pop-up dialog box and click OK

![Figure 19.4.2：KW page－Select Cross reference](.gitbook/assets/2.jpeg)



Save **CSV file**： Keep the default file type-**CSV -** and specify the file name and path.

![Figure 19.4.2：KW page — Save CSV file](.gitbook/assets/3.jpeg)


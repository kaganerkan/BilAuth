
# BilAuth

BilAuth is an authentication system that operates on web-scraping principles. It authenticates users through Bilfen School's student information system.

## How to use

### Downloading Module and Dependencies

You can download the `bilauth` module and its dependencies from PyPI by using the following commands in your command prompt or terminal:

```shell
pip install requests
pip install beautifulsoup4
pip install bilauth
```

These commands will install the necessary packages, including `requests`, `beautifulsoup4`, and the `bilauth` module, which should be available on PyPI. Make sure you have Python and pip installed on your system before running these commands.

### Example Usage and Explanation

```python
from bilauthkaganerkan import bilauth

try:
    # Attempt authentication with a valid TC number and password
    authenticated, data = bilauth.auth(tc="**********", password="example password")
    print(authenticated, data)

except TypeError as e:
    # Authentication failed due to invalid credentials
    authenticated, data = False, {}

except Exception as e:
    # An unexpected error occurred during authentication
    # You can report this issue on GitHub or the appropriate platform
    raise e
```

After running the code like this, the `authenticated` variable will hold the authentication status as a boolean value, and the `data` variable will be a dictionary containing user information. 

For example, if you run this code with a valid password and TC number, the print output will be as follows:

```python
True {'Name': '***** ******', 'School': '***********', 'tc': '**********', 'Password': '********', 'gender': '', 'birthday': '****-**-**', 'schoolno': '***', 'classroom': '**', 'address': '******', 'phonenumber': '********', 'profilepic': 'Userinfo/Profilepic.png'}
```

This output shows that authentication was successful, and it provides details about the authenticated user.
## Legal part


### Is web scraping this website legal?
According to [General Data Protection Regulation Article 6 (a)](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation), as long as the data subject consents to the processing of their personal data, it is considered legal. The information that this package is intended to scrape includes:

- Legal Name & Legal Surname
- High school they are attending
- TC number (This can be considered as the Turkish Citizens' social security number and must be provided already to function; it is not web scraped.)
- Password to the website (This also needs to be provided already to function; it is not web scraped.)
- Gender
- Birthday
- School Number
- Classroom
- Home Address
- Phone Number
- Student's Headshot

Legally, the information subject is not the website itself, but the individual owning the account, in this case, the student who has been given login credentials. **Therefore, you will need the consent of the student, not the website owners. However, it is important to note that using this information in a manner that violates any other rules from the GDPR or similar regulations would be considered unlawful.**

### What Can You Do with Code Licensed Under AGPL 3.0?

Below is a basic list of permissions and restrictions when using software licensed under the GNU Affero General Public License version 3.0 (AGPL-3.0):

**Allowed**:

1. **Use**: You are allowed to use the software for any purpose, whether personal, commercial, or non-profit.

2. **Modify**: You can modify the source code of the AGPL-3.0 licensed software to suit your needs.

3. **Distribute**: You can distribute the AGPL-3.0 licensed software to others.

4. **Run on Your Servers**: You can run the software on your own servers for your organization's internal use without distributing it to others.

**Not Allowed**:

1. **Proprietary Distribution**: You are not allowed to distribute AGPL-3.0 licensed software as a proprietary, closed-source product without also providing access to the source code of the modified version.

2. **Network Use without Source Code Access**: If you use AGPL-3.0 licensed software on a server and provide it as a service over a network (e.g., a web application), you must provide access to the corresponding source code for the modified software to users who interact with it over the network. This includes making source code available upon request.

3. **Removal of License Notices**: You cannot remove copyright notices, disclaimers, or license information from the software's source code or documentation.

4. **Sub-licensing**: You cannot sublicense the software under terms that are more restrictive than the AGPL-3.0 license.

5. **Legal Compliance**: You must comply with all the terms and conditions of the AGPL-3.0 license, including providing access to the source code if required by the license.

6. **Contributions**: If you modify AGPL-3.0 licensed software and distribute your modified version, you must provide access to the source code of your modifications.

7. **No Implied Warranty**: The AGPL-3.0 license does not include any warranties, and you cannot assert that the original authors or contributors endorse or support your modifications or use of the software.

Remember that it's essential to include a copy of the AGPL-3.0 license along with the software when you distribute it. If you have any doubts about compliance, it's advisable to seek legal advice or consult with the project's maintainer.

## User Transparency

### What can a server see when you register with it?

If the code isn't modified or changed to behave differently, the information that will be sent to the server after your login includes:

- Legal Name & Legal Surname
- High school you are studying at
- TC number (Considered as the Turkish Citizens' social security number and must be provided beforehand; it's not obtained through web scraping)
- Password for the website (Must also be provided in advance; it's not obtained through web scraping)
- Gender
- Birthday
- School Number
- Classroom
- Home Address
- Phone Number
- Your Headshot

These are the pieces of information that the server will be able to access. **As the developer of the project, I do not recommend authenticating via Bilauth on a website unless the data storage code is open-source.** Please do not hesitate to report any usage that isn't legal according to the GNU Affero General Public License version 3.0 (AGPL-3.0). Any website or program using this module should make the part containing this module open-source according to this license. However, remember that their data storage code can remain private, so **do not enter your credentials if you have doubts about the site's trustworthiness. Even if it's partially open-sourced, there may still be a part that uses this information unlawfully.**

### How to Ensure Your Data Gets Erased Under GDPR
*(Do note that this isn't a legal advice document)*

As an open-source project, this code or I can't provide assistance, but for getting your data erased, the General Data Protection Regulation (GDPR) has established a set of rules that organizations must adhere to, which include:

1. **Data Necessity:** Personal data should be erased when it is no longer necessary for the purposes for which it was collected or processed.

2. **Withdrawn Consent:** If an individual withdraws their consent, and there is no other legal basis for processing the data, it should be deleted.

3. **Objection:** If an individual objects to the processing of their data, and there are no overriding legitimate grounds for the processing, the data should be erased.

4. **Unlawful Processing:** If data was processed unlawfully, it must be erased.

5. **Legal Obligation:** Data must be erased to comply with a legal obligation.

However, there are exemptions to consider:

6. **Legal Obligations:** Data may be retained if there is a legal obligation to do so, such as for tax or financial reporting requirements.

7. **Contractual Obligations:** Data may not be erased if it is required for the performance of an existing contract between the individual and the company.

8. **Legal Claims:** Data may be retained if necessary for the establishment, exercise, or defense of legal claims.

9. **Public Interest:** Data may not be erased when processing serves a substantial public interest, such as health data for disease monitoring.

10. **Archiving and Research:** Data used for public interest, scientific research, historical research, or statistical purposes may be exempt from erasure.

11. **Freedom of Expression and Information:** Personal data used for journalistic, artistic, or literary purposes may be protected under freedom of expression and information rights.

In most circumstances, individuals have the right to request their data to be deleted. **For more reliable results and to ensure compliance, consider consulting with a legal attorney.**


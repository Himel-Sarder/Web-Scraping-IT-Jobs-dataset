# Web Scraping Job Listings from TimesJobs
![image](https://github.com/user-attachments/assets/af87b8bf-77ac-4c66-9a85-c55673aa69e3)

## Website Link : https://www.timesjobs.com    

## Overview

This project is a Python-based web scraping tool that collects job listings from **TimesJobs** for IT-related positions. It extracts job titles, company names, locations, and experience requirements, and saves the data into a CSV file. The tool uses **BeautifulSoup** and **Pandas** for web scraping and data manipulation.

## Features

- Scrapes job listings from multiple pages of **TimesJobs**.
- Extracts job titles, company names, job locations, and experience requirements.
- Saves the extracted data into a CSV file.
- Handles multiple pages and accumulates data into a single CSV.

## Technologies Used

- **Python 3.x**
- **Libraries:**
  - `requests`: To send HTTP requests and fetch webpage content.
  - `BeautifulSoup (bs4)`: To parse and extract data from HTML.
  - `pandas`: For data manipulation and saving data into CSV.
  - `numpy`: For numerical operations (if needed).

## Sample Output

The script will output a CSV file with the following columns:

- **Job Title**: The title of the job position.
- **Company Name**: The name of the company hiring.
- **Location**: The location(s) of the job.
- **Experience (Years)**: The required experience for the job.

Example output:

| Job Title                          | Company Name                       | Location                     | Experience (Years) |
|------------------------------------|------------------------------------|------------------------------|--------------------|
| Abroad Requirement IT Manager      | RECRUITMENT CANADA IMMIGRATION     | Australia, Canada             | 7 - 12             |
| IT Sales Executive                 | Serviots technology Pvt Ltd        | Ahmedabad                    | 2 - 6              |
| Facilities Manager                 | Sameer namdep Kedari               | Bengaluru, Sibsagar, Patna    | 4 - 9              |
| SAP Experienced Candidates         | TORRENT POWER LIMITED              | Ahmedabad                    | 3 - 5              |

## Troubleshooting

- **403 Forbidden Error**: If you encounter a `403 Forbidden` error, try setting the `User-Agent` header to mimic a browser request:

   ```python
   headers = {'User-Agent': 'Mozilla/5.0 (Windows NT 6.3; Win 64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.162 Safari/537.36'}
   response = requests.get(url, headers=headers)
   ```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

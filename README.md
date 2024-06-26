# SharePointReports - SharePoint Online Reports Script

## Description

This PowerShell script automates data retrieval from the SharePoint Online Admin Center. It efficiently gathers essential information such as site owners, storage quotas, and SharePoint groups for every site collection within your SharePoint environment. The script streamlines this process by exporting the collected data into individual CSV files, providing comprehensive insights that can be easily analyzed or integrated into broader reporting and management workflows. This automation enhances administrative efficiency and ensures accurate documentation of key SharePoint infrastructure details.

## Parameters

- `AdminCenterURL`: The URL of the SharePoint Online Admin Center to connect to.

## Prerequisites

1. **SharePoint Online Management Shell module**: Install using:
   ```powershell
   Install-Module -Name Microsoft.Online.SharePoint.PowerShell

2. **PnP PowerShell module**: Install using: 
   ```powershell
   Install-Module -Name "PnP.PowerShell" -AllowClobber -Force
   Import-Module PnP.PowerShell

3. **Microsoft.Graph module**: Install using:
   ```powershell
   Install-Module Microsoft.Graph -Scope CurrentUser

## Installation - Usage

1. Clone or download the script.
   ```bash
   git clone https://github.com/RapidScripter/SharePointReports.git

2. Open PowerShell with Administrator privileges.

3. Load the script directly using:
   ```powershell
   <path_to_script>\SharePointReports.ps1 -AdminCenterURL "https://example.sharepoint.com"

4. The script generates three CSV files in the script directory. `SiteOwners.csv, SPOStorage.csv and GroupsReport.csv`

## Script Details

### 1. Get Site Owners

- Connects to SharePoint Online and Azure AD.
- Retrieves site owners for each site collection.
- Exports site owners' data to a CSV file.

### 2. Get Site Storage Details

- Retrieves storage quota and usage details for each site collection.
- Exports storage data to a CSV file.

### 3. Get Site Groups

- Retrieves groups and their details for each site collection.
- Exports groups data to a CSV file.

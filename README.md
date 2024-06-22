# SharePointReports - SharePoint Online Reports Script

## Description

This PowerShell script connects to the SharePoint Online Admin Center and retrieves information about site owners, storage quotas, and SharePoint groups for each site collection. It then exports this data into separate Excel files (.CSV).

## Parameters

- `AdminCenterURL`: The URL of the SharePoint Online Admin Center to connect to.

## Prerequisites

1. **SharePoint Online Management Shell module**: Install using `Install-Module -Name Microsoft.Online.SharePoint.PowerShell` if not already installed. 
2. **PnP PowerShell module**: Install using `Install-Module -Name "PnP.PowerShell" -AllowClobber -Force` and `Import-Module PnP.PowerShell` if not already installed.
3. **Microsoft.Graph module**: Install using `Install-Module Microsoft.Graph -Scope CurrentUser` if not already installed.

## Installation - Usage

1. Clone or download the script.
   ```bash
   git clone https://github.com/RapidScripter/SharePointReports

2. Open PowerShell with Administrator privileges.

3. Load the script directly using:
   ```powershell
   <path_to_script>\SharePointReports.ps1 -AdminCenterURL "https://example.sharepoint.com"

4. The script generates three CSV files in the script directory. `SiteOwners.csv, SPOStorage.csv and GroupsReport.csv`

## Script Details

### Parameters

- **AdminCenterURL:** The URL of the SharePoint Online Admin Center.

- **Functions**

#### 1. Get Site Owners

- Connects to SharePoint Online and Azure AD.
- Retrieves site owners for each site collection.
- Exports site owners' data to a CSV file.

#### 2. Get Site Storage Details

- Retrieves storage quota and usage details for each site collection.
- Exports storage data to a CSV file.

#### 3. Get Site Groups

- Retrieves groups and their details for each site collection.
- Exports groups data to a CSV file.

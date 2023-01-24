# MoEWe (Monitoring Environmental Waste Utilization Scores)

A central objective of waste management is to reduce impacts associated with waste generation and treatment to protect human health and the environment. Environmental Waste Utilization quantifies the share of the environmental value of disposed materials which is utilized through waste management. As part of the Environmental Waste Utilization Dashboard (EWU Dashboard) Environmental Waste Utilization scores are calculated to assess the capability of waste management systems to reduce the adverse impacts of waste generation and waste management. The EWU Dashboard enables to explore Environmental Waste Utilization scores for various waste management systems under changing boundary conditions and increases the transparency of indicator calculations. The EWU Dashboard, in form of the “EWU_Dashboard.xlsx”-file, can be shared easily and is accessible also for practitioners or policymakers without profound knowledge of LCA or access to LCA software or databases.
The MoEWe Notebook (MoEWe.ipynb) provides guidance for generating standardized EWU Dashboards based on a spreadsheet template (EWU_InputTemplate.xlsx). MoEWe extensively uses the packages Brightway2 (https://github.com/brightway-lca/brightway2) and “XlsxWriter” (https://github.com/jmcnamara/XlsxWriter) in combination with the ecoinvent database (https://ecoinvent.org/). To observe the effects related to anticipated changes of material and energy systems based on integrated assessment models, MoEWe provides the integration of prospective databases created with the Python package “premise” (https://github.com/polca/premise). The proposed workflow for generating EWU Dashboards is documented below.  

**Generating an EWU Dashboard – The workflow:**  
1.	Use the EWU_Dashboard_InputTemplate.xlsx to gather information (life cycle inventory, life cycle impact assessment methods, background scenarios, …)  
1.1.	To search for activities in the ecoinvent-database, you might use the ecoinvent webversion, the ecoinvent inventory overview (ecoinvent_3.x_cutoff_cumulative_lci_xlsx.7z available via the ecoinvent webpage),or import ecoinvent to any LCA software, such as Brightway2 or the ActivityBrowser).  
1.2.	To search for LCIA methods and elementary flows use the ecoinvent LCIA file (ecoinvent 3.x_cutoff_cumulative_lcia_xlsx.7z available via the ecoinvent webpage) corresponding to your ecoinvent version.   
2.	Generate the EWU Dashboard:   
2.1.	Store all relevant files in a local directory  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.1.1.	InputData.xlsx  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.1.2.	ecoinvent-LCIA-file (ecoinvent 3.x_cutoff_cumulative_lcia_xlsx.7z)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.1.3.	Download and unzip the ecoinvent-Database  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.1.4.	MoEWe.ipynb  
2.2.	Install a Python distribution, such as Anaconda  
2.3.	Create an environment considering the required packages (cf. Requirements.txt) or import the provided environment by following steps 2.3.1-2.3.3.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.3.1.	Store environment.yml in your user directory ("C:\Users\UserName\environment.yml")  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.3.2.	Open Anaconda Prompt  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.3.3.	Enter the command “conda env create -f environment.yml - y”  
2.4.	Run MoEWe.ipynb  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.4.1.	Open Anaconda Prompt  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.4.2.	Activate the MoEWE-environment (“conda activate MoEWe”)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.4.3.	Open Jupyter Notebook (enter the command “jupyter notebook”)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.4.4.	Open MoEWe.ipynb via Anaconda prompt.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.4.5.	Run all. (Correct errors in input data, if needed.)  
3.	After successfully running MoEWe.ipynb the file “EWU_Dashboard.xlsx” is saved in your local directory.  

   
Additional information are available in the associated publication:  
*Schmidt, S.; Laner, D. (in preparation): Environmental Waste Utilization score to monitor the performance of waste management systems*

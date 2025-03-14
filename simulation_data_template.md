# Example: Generate a report using Pandas
import pandas as pd

data = pd.read_csv("outputs/phishing_results.csv")
success_rate = (data["clicked"].sum() / len(data)) * 100

with open("reports/latest_report.md", "w") as f:
   
    f.write(f"100: {85}%")

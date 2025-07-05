This project simulates a **real-time dynamic pricing system** for smart parking lots. It introduces three progressively intelligent pricing models that incorporate factors like occupancy, demand signals, and competitive behavior from nearby lots.

The system is designed to be **data-driven**, **real-time ready**, and **visualized interactively** to provide insights into price changes across different conditions.

1. Data Preprocessing

Combines date and time into a unified column.

Sorts data chronologically by parking lot.

Calculates occupancy rates and encodes categorical features.

2. Model 1 – Linear Pricing
Increases price linearly based on occupancy.

Acts as a baseline model.

3. Model 2 – Demand-Based Pricing
Uses a weighted combination of:

Occupancy

Queue Length

Special Days

Vehicle Types

Nearby Traffic

Demand is normalized and scaled to compute price.

4. Model 3 – Competitive Pricing
Identifies nearby parking lots within 1.5 km.

Adjusts price based on competitor prices at the same timestamp.

Slightly undercuts if they are cheaper.

Slightly raises price if competitors are much more expensive.

5. Streaming Simulation
Uses a generator to simulate real-time data row-by-row.

Designed to plug into a future real-time framework like Pathway.

6. Visualization
Plots prices over time for different parking lots and models using Bokeh.

Allows interactive toggling between models for analysis.

📄 Additional Notes
The system is modular and easily extensible.

Can support real-time input with minimal changes (Pathway, Kafka, MQTT, etc.).

Well-suited for deployment in smart cities, IoT-enabled parking systems, or urban pricing policy tools.

📬 Future Improvements
Integrate real-time data streaming using Pathway or Kafka.

Introduce predictive models using ML (e.g., regression, LSTM).

Deploy as a web app dashboard for live monitoring.





# node-red-heart-monitor-app

This project, Heart Monitor App utilizes Node-RED, a flow-based programming tool, and advanced sensors to provide users with real-time insights into their cardiovascular health. It monitors and analyzes vital signs like blood pressure, heart rate, oxygen saturation, and temperature.


![image](https://github.com/rcseven/node-red-heart-monitor-app/assets/90689825/a6e19762-0e2d-4166-8775-145f91b4e4dd)

The heart monitor app offers a user-friendly dashboard that serves as the central hub for displaying and tracking vital sign data. The dashboard is equipped with interactive graphs and analytics that dynamically visualize the real-time changes in the user's cardiovascular system. These graphs provide a comprehensive overview of the user's health metrics, enabling them to monitor their well-being and make informed decisions about their lifestyle and healthcare.


![image](https://github.com/rcseven/node-red-heart-monitor-app/assets/90689825/6bcd5d25-ac3d-4751-9cda-306bc796aa79)

The blood pressure graph illustrates the user's systolic and diastolic readings over time, allowing them to observe any fluctuations and patterns. The heart rate graph displays the user's heart rate in beats per minute (BPM) and helps track variations during different activities or stress levels. The oxygen saturation graph depicts the user's blood oxygen levels, indicating their respiratory health and efficiency. Lastly, the temperature graph showcases the user's body temperature, giving insights into potential fever or abnormal fluctuations.


![image](https://github.com/rcseven/node-red-heart-monitor-app/assets/90689825/1b758794-3202-42b2-bfd6-1487bdcb4d7a)

If msg.payload is equal to 0, indicating no blood pressure, the status is set to "DEAD ASF" and all pressure variables are set to 0.
If msg.payload is less than 3, indicating low blood pressure (hypotension), the status is set to "Low blood (Hypotension)" and the pressure ranges are adjusted accordingly.
If msg.payload is less than 7, indicating ideal blood pressure, the status is set to "Ideal" and the pressure ranges reflect the ideal values.
If msg.payload is less than 9, indicating high blood pressure (hypertension), the status is set to "High blood (Hypertension)" and the pressure ranges are set accordingly.
If msg.payload is greater than or equal to 9, indicating a critical condition, the status is set to "WARNING!!!" and the pressure ranges are set to higher values.


![image](https://github.com/rcseven/node-red-heart-monitor-app/assets/90689825/668b61e6-98a0-440e-95da-dbb5f7d14079)

If msg.payload is equal to 0, indicating no heart rate, the status is set to "DEAD ASF" and both the minimum and maximum heart rates are set to 0.
If msg.payload is less than 3, indicating a low heart rate (bradycardia), the status is set to "Low (Bradycardia)" and the heart rate range is adjusted with a minimum of 20 and a maximum of 60.
If msg.payload is less than 7, indicating an ideal heart rate, the status is set to "Ideal" and the heart rate range is set with a minimum of 60 and a maximum of 100.
If msg.payload is less than 9, indicating a high heart rate (tachycardia), the status is set to "High (Tachycardia)" and the heart rate range is adjusted with a minimum of 100 and a maximum of 140.
If msg.payload is greater than or equal to 9, indicating a severely high heart rate, the status is set to "Severely High" and the heart rate range is set with a minimum of 150 and a maximum of 200.


![image](https://github.com/rcseven/node-red-heart-monitor-app/assets/90689825/6a3a0e09-151d-4d9c-92a6-0ac59a9977bb)

If msg.payload is equal to 0, indicating no oxygen saturation, the status is set to "DEAD ASF" and both the maximum and minimum oxygen saturation values are set to 0.
If msg.payload is less than or equal to 2, indicating severe hypoxemia, the status is set to "Severe Hypoxemia" and the oxygen saturation range is adjusted with a maximum of 80 and a minimum of 70.
If msg.payload is less than or equal to 4, indicating mild hypoxemia, the status is set to "Mild Hypoxemia" and the oxygen saturation range is adjusted with a maximum of 90 and a minimum of 80.
If msg.payload is less than or equal to 7, indicating an ideal oxygen saturation level, the status is set to "Ideal" and the oxygen saturation range is set with a maximum of 95 and a minimum of 100.
If msg.payload is greater than 7, indicating severe oxygen desaturation, the status is set to "Severe Oxygen Desaturation" and the oxygen saturation range is adjusted with a maximum of 30 and a minimum of 10.



![image](https://github.com/rcseven/node-red-heart-monitor-app/assets/90689825/68a209d6-6a72-466e-935e-331da3cc9883)

If msg.payload is equal to 0, indicating no temperature reading, the status is set to "DEAD ASF" and both the maximum and minimum temperature values are set to 0.
If msg.payload is less than or equal to 2, indicating hypothermia, the status is set to "Hypothermia" and the temperature range is adjusted with a maximum of 30 and a minimum of 25.
If msg.payload is less than or equal to 7, indicating an ideal temperature, the status is set to "Ideal" and the temperature range is set with a maximum of 37 and a minimum of 35.
If msg.payload is greater than 7, indicating a fever, the status is set to "Fever" and the temperature range is adjusted with a maximum of 38 and a minimum of 40.


The Node-RED Heart Monitor App is an invaluable tool for individuals who wish to monitor and manage their cardiovascular health proactively. Whether it's for personal health tracking, fitness optimization, or medical conditions management, this app empowers users to take control of their well-being through real-time data visualization, analytics, and personalized insights.



# SafeMed
SafeMed 💊  SafeMed is a native Android application designed for automated and strict medication tracking. The project is primarily created for the elderly and patients with chronic diseases for whom adhering to a treatment schedule is critical.

The main feature of the app: it doesn't just "ring", but requires mandatory photo-confirmation of the taken pill, followed by the automatic sending of a report to a trusted person (relative or doctor) via Telegram.

🚀 Key Features

⏰ Strict Schedule (Recurrence): Flexible configuration of weekdays and exact time for medication intake.

🛡️ Guaranteed Alerts: Using AlarmManager and Full-Screen Intent allows displaying the alarm window over the system lock, successfully bypassing sleep mode restrictions (Doze Mode).

📸 Photo-confirmation: Integration with the system camera (via FileProvider) and mandatory image cropping using the UCrop library.

✈️ Remote Monitoring: Automatic background sending of a detailed report (Name, medication, status, photo) to a relative's chat using the Telegram Bot API.

🗄️ Local Log (HistoryLog): Reliable transactional storage of the intake history in a local database without the need for constant internet access.

🛠 Tech Stack

Programming Language: Java

Platform: Android SDK (min SDK 24, target SDK 34)

Database: Room Database (SQLite) / Android Architecture Components

Task Scheduler: AlarmManager, BroadcastReceiver

Image Processing: UCrop

Network Interaction: HTTP requests (Telegram Bot API)

File Security: FileProvider (AndroidX)

📱 Screenshots

⚙️ Setup and Installation (For Developers)

Clone the repository:

git clone [https://github.com/Blackbird12356/SafeMed.git](https://github.com/Blackbird12356/SafeMed.git) 


Open the project in Android Studio.

Configure the Telegram Bot:

Create a bot via @BotFather in Telegram.

Copy the generated HTTP API Token.

Paste the token into the corresponding constant in the SmsHelper.java class (or in strings.xml, depending on your implementation).

Build the project and run it on an emulator or a physical device.

👨‍💻 Authors

Developed as part of a course project:

Alisher Olzhasbekov — Product Management, UI/UX, Interface Architecture.

Ramazan Shabalin — Team Lead, Backend logic, Room DB, Telegram API integration, and AlarmScheduler.

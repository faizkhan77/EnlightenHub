# EnlightenHub  

**EnlightenHub** is a dynamic, full-stack web application designed for collaborative learning and discussion. It allows users to create and join topic-specific rooms, engage in real-time conversations, and explore profiles, rooms, and topics, fostering an interactive and productive environment.  

## Features  
- 💬 **Join and create rooms**: Engage in topic-specific discussions.  
- 🖼️ **User profiles**: Customize your profile with an avatar, bio, and see your activity.  
- 🔍 **Search functionality**: Find users, rooms, or topics quickly.  
- 🔄 **Recent activity feed**: Keep track of messages and room interactions.  
- 📚 **Dynamic data handling**: Powered by Django and PostgreSQL for seamless operations.  
- 🔗 **REST API Integration**: Expose key functionalities via APIs for easy access.  
- 📱 **Responsive design**: Optimized for all screen sizes.  

## Project Structure  

```plaintext  
EnlightenHub/  
├── base/                    # App containing core functionalities  
│   ├── templates/           # Inherited HTML pages  
│   └── ...  
├── EnlightenHub/            # Project settings  
│   └── settings.py          # Django settings  
├── media/                   # Uploaded media files (avatars, images)  
├── staticfiles/             # Static files served by Whitenoise  
├── templates/               # Main HTML template  
├── requirements.txt         # Dependencies for the project  
└── manage.py                # Django project management  
```  

## APIs  

The following API endpoints are available:  
- `GET /api`: Base API endpoint.  
- `GET /api/rooms`: Retrieve all rooms.  
- `GET /api/room/:id`: Retrieve a specific room by ID.  

## Technologies Used  
- **Backend**: Django  
- **Database**: PostgreSQL (hosted on Render)  
- **Frontend**: HTML, CSS, JavaScript  
- **Static Files**: Served using Whitenoise  
- **Media Files**: Stored in the `media` folder (optionally can use AWS S3 for persistent storage)  

## Hosting  
- **Website**: Hosted on Render: [EnlightenHub](https://enlightenhub.onrender.com/)  
- **Database**: PostgreSQL hosted on Render  

## Known Limitations  
- **Media Storage**: Media files such as uploaded avatars and images are stored in the `media` folder. Since Render re-deploys the app frequently, these files may be lost. For persistent storage, you can configure **AWS S3** buckets to store and serve media files.  

## Getting Started  

1. **Clone the repository**:  
   ```bash  
   git clone https://github.com/faizkhan77/EnlightenHub.git 
   cd EnlightenHub  
   ```  

2. **Install dependencies**:  
   ```bash  
   pip install -r requirements.txt  
   ```  

3. **Apply migrations**:  
   ```bash  
   python manage.py makemigrations  
   python manage.py migrate  
   ```  

4. **Run the server**:  
   ```bash  
   python manage.py runserver  
   ```  

5. Access the app at `http://127.0.0.1:8000/`.  

## How to Use  
- Create an account or log in.  
- Join rooms of your interest or create new ones.  
- Customize your profile with an avatar and bio.  
- Explore other profiles and their activities.  
- Use the search bar to find rooms, topics, or users.  

## Contributing  
Contributions are welcome! Please fork the repository and create a pull request.  

## License  
This project is licensed under the [MIT License](LICENSE).  

---  
Feel free to update this README as the project evolves!

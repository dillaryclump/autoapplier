This is a undetected web driver that can automate applying for jobs on linkedin and sending cold messages it uses openai api to generate a cover letter.

to use this first add a private file that contains:

mylinkdien.email.example
mylinkdienpassword

then add a apikey file that contains:

myopenapikey

then add your own resume in a docx format the script will automatcially create a new docx file in the output file that automatically inputs the AI generated cover letter into the second paragraph of the docx file
when inputing your own resume name it "Main Resume.docx"

to change the base coverletter that the api edits add your the coverletter varaible (it has my own base coverletter which is a software engineer coverletter)

to choose which jobs you want to automate change this variable in linkedin():     driver.get("https://www.linkedin.com/jobs/search/?currentJobId=3661116542&distance=25&f_AL=true&f_E=2&geoId=103736294&keywords=Junior%20developer&origin=JOB_SEARCH_PAGE_JOB_FILTER&sortBy=R")
choose a linkedin job search with your own settings and search

also change this variable to your own google chrome profile:   options.add_argument("user-data-dir=/home/dillon/.config/google-chrome/'profile 1'")
and change this varaiable to your own chrome executable path:      chromeexecutablepath = "/opt/google/chrome/google-chrome"

now to use the cold message script first run the get_message() and change the companies list to whatever companies you want to search for I have the fortune 500 companys already in there
the get_message() is already looking for recruiters
now the profile links will be stored into the opportunities file then run the process_data_file(filename) with the filename = opportunities this will get rid of profiles that dont accept messages

to change what location you want to contact recruiters with change the keywords list to whatever states or cities you want to message recruiters at
to change the subject that you want to send change the subject.send_keys("Aspiring Software Engineer Intern: Would Love to Connect!") line with what you want to send
same for the message: message_text.send_keys("Hello, I hope this message finds you well. I'm an aspiring software engineer keenly interested in internship/job opportunities. I'd be grateful if you could guide me on any available positions or the application process.Thank you for your time and consideration. Warm regards, Dillon Bishop")




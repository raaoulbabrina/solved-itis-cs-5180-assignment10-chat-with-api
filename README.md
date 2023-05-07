Download Link: https://assignmentchef.com/product/solved-itis-cs-5180-assignment10-chat-with-api
<br>
In this assignment you will get familiar with using with HTTP connections, authentication, and implement an app to share messages. The API details are provided in the Postman file that is provided with this assignment. For authentication you need to pass the token returned from login api as part of the header as described in the Postman file. You should use the OkHttp, GSON and Prettytime libraries.

<table width="612">

 <tbody>

  <tr>

   <td width="229"><strong>API</strong></td>

   <td width="216"><strong>Description</strong></td>

   <td width="61"><strong>Method</strong></td>

   <td width="106"><strong>Requires
 Authentication</strong></td>

  </tr>

  <tr>

   <td width="229"><strong>/api/login</strong></td>

   <td width="216">Login</td>

   <td width="61">POST</td>

   <td width="106">No</td>

  </tr>

  <tr>

   <td width="229"><strong>/api/signup</strong></td>

   <td width="216">Signup</td>

   <td width="61">POST</td>

   <td width="106">No</td>

  </tr>

  <tr>

   <td width="229"><strong>/api/thread</strong></td>

   <td width="216">Get all the threads</td>

   <td width="61">GET</td>

   <td width="106">Yes</td>

  </tr>

  <tr>

   <td width="229"><strong>/api/thread/add</strong></td>

   <td width="216">Add a new thread</td>

   <td width="61">POST</td>

   <td width="106">Yes</td>

  </tr>

  <tr>

   <td width="229"><strong>/api/thread/delete/{thread_id}</strong></td>

   <td width="216">Delete a thread</td>

   <td width="61">GET</td>

   <td width="106">Yes</td>

  </tr>

  <tr>

   <td width="229"><strong>/api/messages/{thread_id}</strong></td>

   <td width="216">Get all message in a thread</td>

   <td width="61">GET</td>

   <td width="106">Yes</td>

  </tr>

  <tr>

   <td width="229"><strong>/api/message/add</strong></td>

   <td width="216">Add a new message to a thread</td>

   <td width="61">POST</td>

   <td width="106">Yes</td>

  </tr>

  <tr>

   <td width="229"><strong>/api/message/delete/{message_id}</strong></td>

   <td width="216">Delete a message</td>

   <td width="61">GET</td>

   <td width="106">Yes</td>

  </tr>

 </tbody>

</table>

<h1>Part A: Login</h1>

This is the launcher screen of you app. The wireframe is shown in Figure 1(a). The requirements are as follows:

<ol>

 <li>The user should provide their email and password. The provided credentials should be used to authenticate the user using the provided login api. Clicking the “Login” button should submit the login information to the api to verify the user’s credentials.

  <ol>

   <li>If the user is successfully logged in then start the Chat Screen, and finish the Login Screen.</li>

   <li>If the user is not successfully logged in, then show a toast message indicating that the login was not successful.</li>

  </ol></li>

 <li>Clicking the “Sign Up” button should start the Signup Screen Figure 1(b), and finish the login Screen.</li>

</ol>

<h1>Part B: SignUp</h1>

Create the Signup screen to match Figure 1(b), with the following requirements:

<ol>

 <li>Clicking the “Cancel” button should finish the Signup Screen and start the Login Screen.</li>

 <li>The user should provide their first name, last name, email, password and password confirmation. Preform the required validation(the given password and the repeated password must match). Clicking the “Sign Up” button should submit the user’s information to signup API.

  <ol>

   <li>If the signup API is not successful display an error message indicating the error message received from the api.</li>

   <li>If the signup API is successful, then store the returned token in the shared preferences, and display a Toast indicating that the user has been created. Then start the Chat Screen and finish the Signup Screen.</li>

  </ol></li>

</ol>

<h1>Part C: Message Threads</h1>

This is the home screen which displays the list of threads as shown in Figures1(c-e) to. Please follow the instructions below:

<ol>

 <li>The top of the screen should display the name of the currently logged in user. The logout button is located in beside the display name.

  <ul>

   <li>Clicking on the ‘logout’ icon should log the user out (delete the token), finish the the screen, and open the login screen.</li>

  </ul></li>

 <li>The list should display the list of message threads. Which should be retrieved using the thread api.

  <ul>

   <li>Clicking on a thread item should open the Chatroom screen of that thread.</li>

  </ul></li>

 <li>The EditText at the bottom of the screen should enable the user to create a new thread.

  <ul>

   <li>After entering the new thread message, the user clicks the add button, which should send the new thread information to the add new thread api.</li>

   <li>After a successful addition of a new thread, the list should be updated to show the updated thread list.</li>

  </ul></li>

 <li>The user should be allowed to delete threads that they have created.

  <ul>

   <li>Display a remove icon beside the title of the threads that were created by the current user. Note: the thread information includes the user_id of the user that created the thread.</li>

   <li>Clicking the remove icon should delete the thread by communicating with the delete thread api. Then the list should be updated to display the updated list of threads.</li>

  </ul></li>

</ol>

<h1>Part D: Chatroom</h1>

This activity displays the list of messages in the particular thread. Also this screen allows the user to add new text messages. The requirements are as follows:

<ol>

 <li>The top of the screen should display the name of the thread as shown in Figure 1(f). Beside the name of the thread there is a home icon button, when clicked should close this activity and display the Message Threads screen.</li>

 <li>For each message display the full name of the user that created the message, the message text, and the time the message was created using the Prettytime Library.

  <ul>

   <li>Display the delete icon only for messages that were posted by the currently logged in user.</li>

  </ul></li>

 <li>The EditText at the bottom of the screen should enable the user to create a new message.

  <ul>

   <li>After entering the new message, the user clicks the add button, which should send the new thread information to the add new message api.</li>

   <li>After a successful addition of a new message, the list should be updated to show the updated message list.</li>

  </ul></li>

 <li>The user should be allowed to delete messages that they have created.

  <ul>

   <li>Clicking the remove icon should delete the message by communicating with the delete message api. Then the list should be updated to display the updated list of message.</li>

  </ul></li>

</ol>

<strong>Good Luck!</strong>
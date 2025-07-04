// Supabase setup
const SUPABASE_URL = ' 'https://wlthlwxcmltwescezjlk.supabase.co'; // ⬅️ Replace with your Supabase URL
  
const SUPABASE_KEY = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6IndsdGhsd3hjbWx0d2VzY2V6amxrIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NTE0NDQ4MDcsImV4cCI6MjA2NzAyMDgwN30.tvUeTFVDdQomDHHV0JSpsXHP9IbQVkOhEvBpCglzI-o';
const supabase = supabase.createClient(SUPABASE_URL, SUPABASE_KEY);

// Display forms
function showRegister() {
  document.getElementById('formContainer').innerHTML = `
    <form onsubmit="registerUser(event)">
      <h3>Register</h3>
      <input type="email" id="regEmail" placeholder="Email" required />
      <input type="password" id="regPassword" placeholder="Password" required />
      <button type="submit">Register</button>
    </form>
  `;
}

function showLogin() {
  document.getElementById('formContainer').innerHTML = `
    <form onsubmit="loginUser(event)">
      <h3>Login</h3>
      <input type="email" id="loginEmail" placeholder="Email" required />
      <input type="password" id="loginPassword" placeholder="Password" required />
      <button type="submit">Login</button>
    </form>
  `;
}

// Register User
async function registerUser(e) {
  e.preventDefault();
  const email = document.getElementById('regEmail').value;
  const password = document.getElementById('regPassword').value;

  const { user, error } = await supabase.auth.signUp({ email, password });

  if (error) {
    alert('Registration error: ' + error.message);
  } else {
    alert('Check your email to confirm your registration.');
  }
}

// Login User
async function loginUser(e) {
  e.preventDefault();
  const email = document.getElementById('loginEmail').value;
  const password = document.getElementById('loginPassword').value;

  const { user, error } = await supabase.auth.signInWithPassword({ email, password });

  if (error) {
    alert('Login error: ' + error.message);
  } else {
    alert('Welcome! Login successful.');
  }
}

.. admonition:: Course is live
   
   .. raw:: html

      <div style='margin-top:.4em; margin-bottom:0em'><i><span id="lastModified"></span></i></div>

      <script>

      const options = {
      weekday: "short",
      year: "numeric",
      month: "short",
      day: "numeric",
      };

      // Get the raw last modified string (e.g., "07/26/2014 23:54:23")
      const modifiedDateString = document.lastModified;
      var lastModDate = new Date(document.lastModified);
      // Create a JavaScript Date object from the string
      const dateObj = new Date(modifiedDateString);

      // Format the date object to show only the time (hours and minutes)
      // This uses the user's local time zone and format (e.g., 11:54 PM or 23:54)
      const formattedTime = lastModDate.toLocaleDateString('en-US', options) + " at " + dateObj.toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' });

      // Display the result in the HTML element
      document.getElementById("lastModified").textContent = "Last updated " + formattedTime;
      </script>   
# Menus Bug Report

-----------------------

## Survival Menu

### /bank

-- The /bank portion is disabled/is not functional. Game states that the command is unknown and it seems as though it is just the command, this includes the icon in the survival menu being disabled due to it running the same in-game command even when I try to type it in manually I still get the Same error. ~ Sent (07/02/25 @ 6:35pm{EST}) - By: KS43

## /jobs

-- The Jobs "LumberJack", "Miner", "Builder", "Craftsman", "Excavator", " " Does not payout to the player in any capacity, and doesnt seem to be working properly. The /Jobs menu works, the /jobs info panel works, and I can even select a job. But the money that should be being earned from that job is not being given to the player.  ~ Sent (07/02/25 @ 6:35pm{EST}) - By: KS43

# ⚡ Meeting Time Converter

Hey team — I’ve scheduled our meeting for **6:15 PM EST**. Below is the button to view it in *your* local time.

**EST (New York)** Meeting Time:  
**6:15 PM**

<button id="convert-btn">Show me my local time</button>

<p id="local-time"></p>

<script>
  // Base time as EST (UTC-5)
  const baseEST = "18:15"; // HH:mm in 24h format
  const [h, m] = baseEST.split(":");
  
  document.getElementById("convert-btn").onclick = () => {
    // Build a date object using today's date and EST base time
    const now = new Date();
    // Create in UTC, then shift to EST by subtracting 5h
    const utcStamp = Date.UTC(
      now.getFullYear(),
      now.getMonth(),
      now.getDate(),
      parseInt(h, 10) + 5,  // EST is UTC‑5, so add 5 to get UTC
      parseInt(m, 10)
    );
    const localDate = new Date(utcStamp);
    
    // Format local time
    const opts = { hour: '2-digit', minute: '2-digit', hour12: true, timeZoneName: 'short' };
    const localStr = localDate.toLocaleTimeString(undefined, opts);
    
    document.getElementById("local-time").innerText =
      `Your local time: **${localStr}**`;
  };
</script>

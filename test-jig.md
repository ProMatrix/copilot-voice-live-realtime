Run `developer-assistant` first.

Do exactly this:

1. Start `host-gemini-voice`.
2. Open the `developer-assistant` profile.
3. Click `Start Recording`.
4. If the assistant speaks first, let her finish completely.
5. Then say one short prompt into the microphone, about 5 to 10 seconds.
Example: “Explain closures in JavaScript with a simple example.”
6. Stop speaking and wait until:
   - the user transcript appears, and
   - the assistant starts responding, or
   - it clearly stalls.
7. Do not keep talking. Do not do a second turn.
8. Look at the `Realtime Diagnostics` panel on the right.
9. Click `Download JSON`.
10. Send me that JSON file, or paste its contents here.

That is all I need for the first pass.

What I want from that one run:
1. `Mic Max Gap`
2. `Send Max Gap`
3. `Max Encode`
4. `Stop -> User`
5. `Stop -> Assistant`
6. `Last Audio -> Transcript`
7. the short event list from the diagnostics JSON

Do not stop the session before the assistant has at least started replying, unless it is obviously hanging. I need the first full user turn, not just the recording start.

Do not run `programming-essentials` yet. I want `developer-assistant` first because it removes the PDF variable from the first diagnostic capture.

If you cannot or do not want to send the JSON file, then send these exact values from the panel:
1. `Mic Chunks`
2. `Mic Max Gap`
3. `Sent Chunks`
4. `Send Max Gap`
5. `Max Encode`
6. `Stop -> User`
7. `Stop -> Assistant`
8. `Last Audio -> Transcript`
9. each line in the event list

After that, I will tell you whether to run `programming-essentials` as the second comparison.
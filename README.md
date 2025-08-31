[README.md](https://github.com/user-attachments/files/22068492/README.md)
# VAPI Hybrid Chat Widget - Premium Voice + Text

A premium customizable text + voice chat widget that integrates with VAPI AI assistants. Users can seamlessly switch between typing and speaking with your AI assistant.

## Features

- ✅ **Dual Mode**: Text chat AND voice chat in one widget
- ✅ **Premium Voice Button**: Beautiful animated button with state changes
- ✅ **Separate Transcripts**: Text and voice conversations in separate windows  
- ✅ **Seamless Switching**: Toggle between text and voice mid-conversation
- ✅ **Voice Visualization**: Real-time button animations and status updates
- ✅ **Smart Permissions**: Handles microphone access gracefully
- ✅ **Conversation Context**: Maintains context across text and voice
- ✅ **Clean UI**: Professional interface that matches your brand
- ✅ **No CSS Conflicts**: Fully isolated styling
- ✅ **Mobile Friendly**: Responsive design for all devices
- ✅ **Easy Integration**: Just 3 files and 5 minutes setup

## Premium Voice Features

- **Premium Button Design**: Green with pink text, no microphone icon
- **State Animations**: Orange glow when connecting, red pulse when active
- **Conversation Pulse**: Button pulses with speech patterns
- **Separate Transcripts**: Voice and text conversations are visually distinct
- **Clean Transcription**: No duplicate messages, final transcripts only

## Quick Setup

1. **Get your VAPI credentials:**
   - Public Key (for voice calls)
   - Private Key (for text API calls) 
   - Assistant ID

2. **Upload files to your website:**
   - `vapi-hybrid-widget.html` - The widget HTML structure
   - `vapi-hybrid-widget.css` - All styling with premium animations
   - `vapi-hybrid-widget.js` - Functionality and API integration

3. **Add to your website:**
   ```html
   <!-- Add before closing </body> tag -->
   <link rel="stylesheet" href="vapi-hybrid-widget.css">
   <div id="vapi-hybrid-widget-container"></div>
   <script src="vapi-hybrid-widget.js"></script>
   <script>
     VapiHybridWidget.init({
       privateKey: 'your-private-key',
       publicKey: 'your-public-key', 
       assistantId: 'your-assistant-id',
       title: 'Chat with Alex',
       primaryColor: '#034537',
       accentColor: '#f5ced5'
     });
   </script>
   ```

## Configuration Options

```javascript
VapiHybridWidget.init({
  // Required
  privateKey: 'your-vapi-private-key',    // For text chat API
  publicKey: 'your-vapi-public-key',      // For voice calls
  assistantId: 'your-vapi-assistant-id',
  
  // Optional customization
  title: 'Chat with us',                  // Header title
  subtitle: 'How can we help?',           // Initial text message
  voiceWelcome: 'Ready to chat?',         // Initial voice message
  primaryColor: '#034537',                // Main brand color
  accentColor: '#f5ced5',                // Secondary color
  position: 'bottom-right',               // Widget position
  size: 'normal',                         // 'compact' or 'normal'
  defaultMode: 'text'                     // Start in 'text' or 'voice' mode
});
```

## Usage Modes

### Text Chat Mode
- Type messages like traditional chat
- Full conversation history
- Works on all devices and browsers
- Clean message bubbles with your brand colors

### Voice Chat Mode  
- Click the premium "Start Call" button
- Real-time voice status updates and animations
- Beautiful button state changes (green → orange → red)
- Button pulses with conversation flow
- Separate transcript window with premium styling
- Automatic microphone permission handling
- Voice-to-voice AI conversations

### Hybrid Usage
- Start in text, switch to voice anytime
- Separate conversation windows for each mode
- Perfect for accessibility and user preference
- Context maintained across both modes

## Premium Voice Button States

1. **Default**: Green button with pink "START CALL" text
2. **Connecting**: Orange glow with "CONNECTING..." text
3. **Active**: Red gradient with "END CALL" text + pulse animation
4. **Listening**: Extra pulse animation when user speaks
5. **Assistant Speaking**: Smooth animation when AI responds

## Client Customization

For each new client:

1. Replace the VAPI credentials (private key, public key, assistant ID)
2. Update colors to match their brand
3. Change the title and messaging (including voice welcome message)
4. Optionally adjust positioning and size

## Styling Customization

### Button Colors
Find these lines in `vapi-hybrid-widget.css`:
```css
--vapi-primary-color: #034537;  /* Main widget color */
--vapi-accent-color: #f5ced5;   /* Button text color */
```

### Voice Messages
Change the initial voice message in the HTML file:
```html
🎤 Voice chat ready - click the button below to start your conversation
```

### Connection Message
Change the connection message in the JavaScript file:
```javascript
addVoiceMessage('system', '🎤 Voice call connected - speak now!');
```

## Security Note

⚠️ **Important**: The private API key is exposed in client-side code. For production use, consider:

1. Creating a backend proxy endpoint
2. Using environment variables
3. Implementing proper API key rotation

## Files Included

- `README.md` - This setup guide
- `vapi-hybrid-widget.html` - Widget HTML structure  
- `vapi-hybrid-widget.css` - All styling with premium animations
- `vapi-hybrid-widget.js` - Core functionality (text + voice)
- `demo.html` - Working example
- `integration-examples/` - Platform-specific examples

## Integration Examples

See the `integration-examples/` folder for:
- Shopify theme integration (complete theme.liquid)
- WordPress plugin format
- React component version
- Plain HTML website integration

## Browser Support

- **Text Chat**: All modern browsers
- **Voice Chat**: Chrome, Firefox, Safari, Edge (requires HTTPS)
- **Mobile**: Responsive design works on all devices

## Troubleshooting

### Voice Issues
- Ensure you're using HTTPS (voice requires secure connection)
- Check microphone permissions in browser
- Verify public key is correct for voice calls

### Text Issues  
- Check private key is correct for API calls
- Verify assistant ID matches your VAPI setup
- Check browser console for API errors

## Support

For questions or customization requests, contact the developer.

---

*Built with VAPI AI Platform - Premium Hybrid Widget Package*

# Node-Red
Quality Node-Red nodes
<p>
        This node uses <a href="https://aws.amazon.com/polly/">Polly</a> TTS api and Node Sonos api.
    </p>
    <p>
        This is a very early alpha, so use at your own risk.<br/>
    </p>
    <p>
    USE: Set the configuration of Polly (you need the free Amazon AWS credentials), then set your Sonos IP Address (Sonos
    doesn't allow to set a fixed IP to the sonos's device, so you need to reserve an IP using the DHCP Reservation function of your
    router/firewall's DHCP Server).
    </p>
    <p>
    Send to the node, a payload with the text you want to speed out. For example <code>{payload:"Hello there!"}</code>.<br/>
    You can send multiple messages at once. The node will handle the queue.
    </p>
    <br/>
    <p>
    Known issues:<br/>
    If the Sonos device is set to LineIn, TVin or other physical input, the node doesn't work. You need to play something via Sonos App, then stop the play. Then the node will work again
        <br/>
        If some music is playing, the node will wait for the music to stop, before playing the TTS message.
    </p>
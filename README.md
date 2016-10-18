1. Need to install PyAudio PyAudio 0.2.9+ 
           
    sudo apt-get install portaudio19-dev python-all-dev python3-all-dev && sudo pip install pyaudio

Download https://pypi.python.org/pypi/PyAudio#downloads (PyAudio-0.2.9.tar.gz), then unzip and go to the PyAudio-0.2.9 folder and run this command
                 
                 sudo python setup.py install
                 
More information: https://github.com/Uberi/speech_recognition

2. This will show information of all the plugged devices

                    import pyaudio;
                    audio=pyaudio.PyAudio();
                    print([audio.get_device_info_by_index(i) for i in range(audio.get_device_count())])

Sample output

                    {
                    'defaultSampleRate':44100.0,
                    'defaultLowOutputLatency':0.008707482993197279,
                    'defaultLowInputLatency':0.008707482993197279,
                    'maxInputChannels':1L,
                    'structVersion':2L,
                    'hostApi':0L,
                    'index':1,
                    'defaultHighOutputLatency':0.034829931972789115,
                    'maxOutputChannels':2L,
                    'name':u'USB PnP Sound Device: Audio (hw:1,
                    0)', 'defaultHighInputLatency':0.034829931972789115
                    }

Some useful information:

http://dsp.stackexchange.com/questions/33719/how-to-match-a-piece-of-very-short-audio-based-on-key-and-pitch-to-find-a-piece/33721#33721

http://dsp.stackexchange.com/questions/33719/how-to-match-a-piece-of-very-short-audio-based-on-key-and-pitch-to-find-a-piece (this will help us to get going...)

http://stackoverflow.com/questions/6170548/using-python-to-measure-audio-loudness

http://stackoverflow.com/questions/13329617/change-the-volume-of-a-wav-file-in-python


3. To install SoundAnalyse

        git clone https://github.com/ExCiteS/SLMPi/tree/master/SoundAnalyse-0.1.1
        
   Once it downloaded go to the SLMPi/SoundAnalyse-0.1.1 and run this command
   
         sudo python setup.py install

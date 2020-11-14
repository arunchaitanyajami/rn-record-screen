# rn-record-screen

rn-record-screen

## Installation

```sh
npm install rn-record-screen react-native-record-screen react-native-ffmpeg
```

## Usage

```js
import { useRecordScreenZone } from 'rn-record-screen';

export const App = () => {
  const { startRecording, stopRecording, RecordScreenZone } = useRecordScreenZone();

  const _handleOnStartRecording = () => {
    startRecording({mic: true})
  }

  const _handleOnStopRecording = async () => {
    const res = await stopRecording()
    if (res) {
      console.log(res)
    }
  }

  return (
    <>
      <Navbar />
      <View>
        <View>
          <Text>Not recording area<Text>
        </View>
        <RecordScreenZone>
          <View>
            <Text>Recording area<Text>
          </View>
        </RecordScreenZone>
      </View>
      <Footer />
    </>
  )
}
```

## License

MIT

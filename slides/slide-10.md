### ReactJS and Functional Programming

Functional components

````typescript
const AlertMessage = ({message}:{message: string}) => <div className="message">{message}</div>
````

Functional composition using hooks

````typescript
const AlertMessageFromCode = ({code}:{code: number}) => {
    const { translate } = useTranslateCode();
    return <div className="message">{translate(code)}</div>
}
````

Immutability, kind of...

````typescript
const AlertMessageFromCode = ({code}:{code: number}) => {
    const [ message, setMessage] = useState();
    const { translate } = useTranslateCode();
    const handleClick = async () => {
        const message = await translate(code);
        setMessage(message);
    }
    return <div className="message" onClick={handleClick}>{message || code}</div>
}
````

